# SpongeZoneTools
Plugin designed to augment the [official InfiltrationEngine tooling](https://github.com/MoonstoneSkies/InfiltrationEngine-Custom-Missions) and any derivative plugins.

Currently consists of three tools:
1) Cell Fixup - One-press button to fix styling of manually produced cell floors/ceilings, as a bonus also consistently styles Links
2) Toggle Group Visibility - Non-destructively toggles the visibility of an entire model/folder, a'la blender's collection visibility
3) [Attribute Importer](#attribute-importer)

Use at your own risk etc. etc.

## Attribute Importer
The attribute importer is a tad more elaborate than the other tools so it's getting its own dedicated section  

The attribute importer performs four functions, each mapped to one of the buttons shown when clicking on the "Attribute Importer" button in the toolbar. They are as follows:

### 1) Import Non-Global Attributes
Creates every attribute specific to each selected item (prop/statecomponent/bot/link etc.) provided the attribute doesn't already exist  
**Examples of non-global attributes** are the `DifficultDrill` attribute on doors, or the `Path` attribute on Links  

### 2) Import Global Attributes
Creates every attribute that isn't specific to a single item for each item in the selection provided the attribute doesn't already exist  
**Examples of global attributes** are the `Color0` attribute used for re-colouring props, or the `Tag` attribute used for accessing props from `StateScript`s

### 3) Import All Attributes
Performs the function of both of the prior options at the same time

### 4) Delete All Attributes
Deletes **EVERY** attribute on every item in the selection, regardless of wether each attribute was created via the importer or not

All of the above functions with the exception of the "Delete All Attributes" tool work on `Links`, `Bots`, `ConditionalGeometry`, `Glass`, most `Prop`s, and most `StateComponent`s, the Delete All Attributes tool functions regardless of selection