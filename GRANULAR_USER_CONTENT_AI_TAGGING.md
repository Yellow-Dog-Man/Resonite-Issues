# Granular AI tagging of user generated content
This is an accompanying document for the (Generative AI disclosure policy for user content)[USER_CONTENT_AI_POLICY.md], describing how to use the detailed tagging options of `AI_GeneratedContent` component.

As stated in the policy, detailed tagging is **FULLY OPTIONAL** and not required to comply with the policy. However when in use, must fully cover the actual usage.

However providing detailed information has a number of benefits:
- Content will be visible to more users
- More content will be considered for featuring
- Users will be able to better understand how the technology was actually used

## What happens without granular tagging?
When any granular tagging information is missing, user content filters will assume highest level of usage for given aspect of the content and filter it.

Default `AI_GeneratedContent` component applies generic AI tag, which will **always be filtered** when user has filtering enabled. 

Additional detail can let the content through user's filters if they indicates that they are fine with given level of usage.

### Hierarchy percetange
Easiest way to provide more detail about usage is to indicate how much of the content's hierarchy is affected by use of generative AI. You do not need to calculate this value manually - it will be done automatically when the item/world is saved.

To allow this percentage to be calculated, following criteria must apply:
- Switch `TagScope` value from `Global` to `ChildHierarchy`
- Ensure the tag is present **on the roots** of all affected hierarchy
    - In other words, all content made with generative AI must always be **under** `AI_GeneratedContent` component with this scope
    - You can place as many `AI_GeneratedContent` components in the hierarchy - the better the AI content is separated, the more accurate the calculated percentage can be
    - This excludes any Resonite-managed hierarchies that you don't have control over
- There are no instances of `AI_GeneratedContent` with `TagScope` set to `Global` in the saved hierarchy

When saving content (items or worlds), Resonite will calculate number of slots under `AI_GeneratedContent` component and outside to compute the final ratio. Slots with no components present on them are ignored for this purpose.

The goal of this filter is to understand how much content is roughly made with generative AI. E.g. a world made mostly without generative AI with only few objects will show that only small percentage of the hierarchy is tagged, removing ambiguity on the level of use.

When filtering content, this aspect takes highest precedence and will allow content through if it's below the percentage set by user, even if it would not pass other filters.

Importantly, this filter also works even if **no other detailed information is provided**, making this the easiest way to provide fine grained filtering.

### Detailed AI usage
Next step in providing detailed information is to add details on the specific usage of generative AI. This is also fully optional, regardless of whether hierarchy percentage tagging was used or not.

During filtering, this information can let content through a filter, even if it would not pass hierarchy percentage filter.

To provide detailed AI usage, do following:
- On the `AI_GeneratedContent` add a new entry to `UsageDetails` list
- (Optional) Fill out `ToolName` with the name of the tool / model used
- (Optional) Fill out `Description` with verbal description on how the technology was used
- Correctly indicate usage for the specific use:
     - `Translation` - check if generative AI was used for translation
     - `LiveInteraction` - check if your content interfaces with generative AI functionality
     - Indicate highest level of usage (see below) depending on the type of content:
        - `TextUsage` - user readable text, **NOT** including translation
        - `ImageUsage` - image assets, textures, sprites
        - `AudioUsage` - audio assets such as sound effects, ambiance or music, **EXCLUDING** audio tracks in video assets
        - `VideoUsage` - video assets (with or without audio track)
        - `ModelUsage` - 3D models, points clouds, gaussian splats and other analogous model assets
        - `SceneUsage` - Object / Scene hierarchy & structure, **EXCLUDING** usage necessary to simply represent other types e.g. asset providers and ProtoFlux
        - `CodeUsage` - generated code, such as ProtoFlux, WASM and so on

You can add multiple instances of `UsageDetails` if you wish to separate the usage per each tool used. However a single entry with aggregate information is also acceptable.

#### Highest level of usage
Indicating content usage is done in several levels, depending on how generative AI was used. These are defined as follows, in increasing level of use:

- **None** - No generative AI functionality was used for the content
- **Concepts** - sketches, concepts, or other materials were used as a basis for the content, but the final content itself was human made
- **Modifications** - when pre-existing human made content was partially modified with AI
- **Generation** - when the entire content is fully generated by AI

While tagging, you need to indicate the highest level usage for any final piece of content present.

For example:
- If all image assets were made by you based on sketches generated by AI, highest usage level is `Concepts`
- If you used AI to partially modify some of the image assets you made, highest usage level is `Modifications`
- If you prompted AI to generate some of the image assets, the highest level is `Generation`
    - It does not matter what form the prompt was - whether it was text or other image assets
    - It does not matter if you modify the assets afterwards, as long as parts of the generated image remain

When filtering, users indicate which level of usage they want to allow through the filter.

E.g. users with filter `ImageUsage`set to `Modifications`, will see content tagged with `None`, `Contepts` and `Modifications`, but not `Generation`.

In order to pass through the filter, all types of content must pass.

E.g. users with filter `AudioUsage` set to `Generation` and `ImageUsage` set to `Modifications`, will **NOT** see content that has both `AudioUsage` and `ImageUsage` indicated as `Generation.