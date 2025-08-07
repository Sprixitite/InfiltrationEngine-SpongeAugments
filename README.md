# InfiltrationEngine // SpongeAugments
Plugin designed to augment the [official InfiltrationEngine tooling](https://github.com/MoonstoneSkies/InfiltrationEngine-Custom-Missions) and any derivative plugins.

Use of this plugins is at your own risk

Currently consists of three tools:
1) [Attribute Importer](#attribute-importer)
2) [One-Click Tools](#one-click-tools) - A collection of small assorted tools usable in a single click
3) Toggle Group Visibility - Non-destructively toggles the visibility of an entire model/folder, a'la blender's collection visibility

### Now With A Settings Menu!
The settings module allows you to configure the plugin, currently allows disabling the One-Click menu and placing the associated tools in the main toolbar

### Now Supports Light Mode!
If you asked for this, my Ko-Fi is linked for a reason because man was this awful to implement  
I kid, of course - at least about the donations part

## Attribute Importer
The attribute importer is a tad more elaborate than the other tools and is probably the main reason you're using the plugin to begin with

The attribute importer performs five functions, each mapped to one of the buttons shown when clicking on the "Attribute Importer" button in the toolbar. They are as follows:

### 1) Import Non-Global Attributes
Creates every attribute specific to each selected item (prop/statecomponent/bot/link etc.) provided the attribute doesn't already exist  
**Examples of non-global attributes** are the `DifficultDrill` attribute on doors, or the `Path` attribute on Links  

### 2) Import Global Attributes
Creates every attribute that isn't specific to a single item for each item in the selection provided the attribute doesn't already exist  
**Examples of global attributes** are the `Color0` attribute used for re-colouring props, or the `Tag` attribute used for accessing props from `StateScript`s

### 3) Import All Attributes
Performs the function of both of the prior options at the same time

### 4) Delete Imported Attributes
Deletes every known global/private attribute on every item in the selection, regardless of whether each attribute was created via the importer or not

### 5) Delete All Attributes
Deletes **EVERY** attribute on every item in the selection, regardless of whether each attribute was created via the importer or not

All of the above functions with the exception of the "Delete All Attributes" tool work on `Links`, `Bots`, `ConditionalGeometry`, `Glass`, CustomProp `Motor`s, Prop Override `Base` parts, most `Prop`s, and most `StateComponent`s, the Delete All Attributes tool functions regardless of selection

## One-Click Tools
The one-click tools menu is designed to contain any small tools operable in a single button press. Currently it contains two tools:

### 1) Child Organizer
Organizes the children of all selected instances alphabetically. Useful for decluttering the hierarchy of custom props

### 2) Generate Slope Part
For every selected Wedge, generates a part completely covering the wedge's slope

### 3) Cell Fixup
Upon use, fixes the styling (colour, materials, transparency, etc.) of all `Cell`s and `Link`s found within the current place file

### 4) Custom Prop Base Generator
Upon use, creates a new "Base" part in every selected model where one does not exist. Then readjusts the "Base" part in every selected model to the bounding box of the model