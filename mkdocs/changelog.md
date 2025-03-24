# Changelog

## Release Note Zen Sets 2.4.5
### New
1. Added support for **Blender 4.4**

## Release Note Zen Sets 2.4.4
### New
1. Horisontal button layout in Combo Panel

### Enhancement
1. Iterate Zen Sets object modes by `Shift+Ctrl+Wheel Up/Down`
2. Option to alternatively set Collection Parent Selector by `Shift+Ctrl+Wheel Up/Down`

### Fix
1. Tweak and select mode panel was missing in Zen Sets workspace tool

## Version 2.4.3

### New:
1. Added support for **Blender 4.3**
2. Generic "Iterate Groups" operator
3. Attributes in "Sets" mode are synchronized with group name (for better Geometry Nodes support)

#### Enhancement:
1. Option to switch off Gizmo Help Button in Preferences
2. Keymap collision indication

#### Fix:
1. Can not group similar mesh by material in "Auto Groups" operator in Blender greater 4.0
2. Pie assist is not working in Blender 4.3
3. Object collections mode is not working in Blender 4.3

## Version 2.4.2

#### Fix:
1. Geometry Node Tools were broken for Blender 4.2

## Version 2.4.1

### New:
1. Option to change N-Panel name from "Zen Sets" to "Zen"

#### Enhancement:
1. Right menu extended items can be switched off in Preferences

#### Fix:
1. Sculpt group operations corrected for Blender 4.2


## Version 2.4

### New:
1. Custom scripts
2. Nova Export

#### Enhancement:
1. Option to convert multiple parent objects to collections
2. Batch rename by variables
3. Auto groups by parent objects with hierarchies
4. Ignore scrolling collections in tool mode
5. Apply modifiers and transforms before Join objects
6. Option to work with Zen Sets in background mode

#### Fix:
1. Tool scroll not working when some collections are isolated
2. Delete group with "Hierarchy" option does not work in Object Parts mode
3. New group name by active object didn't work properly

## Version 2.3

### New:
1. Blender 4.0 Support
2. Example Panel

#### Tools:
1. Mesh groups to islands
2. Change group ID

#### Import-Export:
1. Blender Sculpt Face Sets
2. Blender 4.0 Face Maps Attribute
3. Blender Integer Attributes

### Geometry Nodes:
1. Value To Color Node
2. Select By Group ID Node
3. Group Name To ID Node
4. Panel in Geometry Node Editor N-Panel

## Version 2.2.2

### New:

#### UI List:
1. Option to select multiple groups in list

#### Tools:
1. Rename mesh groups by material

#### Display:
1. Option to switch off display in View3D and activate only in UV

### Fix:
1. Wrong hierarchy of child-parent objects
2. Text, metaball objects were not shown
3. Mesh groups filtering and sorting were not working properly
4. Ensure active object in Group Selector caused error in mesh selector

### Enhancement:
1. Option to change default groups list and objects list row count in preferences
2. AutoGroups multi object fix, added presets: Similar by normal, Similar by material

---

## Version 2.2

### New:

#### Draw:
Python BGL module was replaced with GPU

#### UI:
1. New compact user interface
2. Addon popup menu
3. Object Panel

#### Object Panel:
1. Display objects of the active group
2. Multiple object filters:
   - show objects with different properties (Example: Disable in Renders != Disable in Viewport)
3. Display objects in Edit Mode with the option to center selected object in the viewport
4. Filter objects with unique data

#### Tools:
1. Make a group from objects visible to the active camera
2. Select objects visible to the active camera
3. Add materials to collections

### Enhancement:
1. Adopt the name of the active object when new group is created
2. Option to select object collection if active object is linked to multiple collections
3. Ensure active object in Group Selector
4. Option to delete all empty objects when parent object is converted to collection

---

## Version 2.1.0

### New:
#### List Options:
1. Display only active object collections

#### Tools:
1. Set active collection parent or child in 3D View and select all its objects
2. Join objects in group and optionally mark them as Zen Sets face, vert parts or Blender face maps

### Enhancement:
1. Group common preferences by tabs

---
## Version 2.0.2

### New:
#### List Options:
1. Total area in Face Group
2. Total perimeter in Face Group
3. Total edge length in Edge Group

### Fix:
1. Import Vertex Colors - was not working for Vertex Groups and Face Maps

---
## Version 2.0.1
### New:
#### Pie Menu:
1. Rename Group (Collection)
#### Sculpt
1. Add, Replace, Subtract and Intersect Sculpt Mask from any Zen Sets Group or Blender Vertex Group and Face Map
2. Save Sculpt Mask to Vertex Group
3. Toolbar in Sculpt Mode
4. Vertex Group to Sculpt Mask Panel
#### Tools
1. Batch Rename Preview and support of regular expressions

### Enhancement:
1. Object Parts draw 2x faster

### Fix:
1. Delete All Collections caused error

---
## Version 2.0
### New:

#### 1. Vertex Groups and Face Maps Support in Zen Sets
##### 1.1. Display System
- Highlight Vertex Groups and Face Maps with Zen Sets overlay
##### 1.2. Pie Menu
Besides standard Zen Pie Menu options to toggle hide, select, append-remove etc.:
- Display Weights
- Assign
- Isolate|Restore Group with option to use Mask Modifier to hide in Object Mode
##### 1.3. WorkSpace Tool
- Full tool support for Blender Vertex Groups and Face Maps in the same way as Zen Sets Groups
##### 1.4. Tools
Support of standard Zen Sets mesh element tools like 'Batch rename Groups', 'Create Objects from Groups' etc. and additional:
- Remove vertices with given Weight Range from Group
- Set Sculpt Mask
##### 1.5. N-Panel
- Vertex Groups and Face Maps hidden state, elements count
- Vertex Weight monitor and status icon
- Vertex Weight to Color converter and back
- Vertex Weight Presets
- Copy-Paste between all mesh Zen Sets modes

#### 2. Object mode new features
##### 2.1. Display System
- Display active Object name and names of its user Collections (Groups)
- Option to display names of all Collections (Groups)
- Selected Collection indicator
##### 2.2. Pie Menu
- Remove selected from all Groups
##### 2.3. Tools
- Sort collections
- Select Objects with Vertex Groups, Face Maps, Modifiers
##### 2.3. N-Panel
- Disable in Renders indicator and monitor
- Remove selected from all Groups
- Remove Objects with linked data from Groups

### Enhancement:
1. Hide objects after append to hidden Object Set
2. Hide viewport, hide select and other status indicator detect object state also
3. More performance in Edit Mesh mode
4. If Zen Sets mode is switched off now, it speeds up total addon performance
5. Option to Copy Groups with filter by name

### Fix:
1. Filters in UI Lists were not working

---
## Version 1.4.1
### New:
#### Tools:
* Rename Objects as Collection operator.
* Rename Collection as Object operator.

### Fix:
* Fixed Create Objects from Groups in Multi object mode.

---
## Version 1.4
### New:

#### 1. Simple Object Sets and Parts
- Highlight Zen Sets Simple Object Sets and Parts
- Integration to all Zen Sets instruments: UI List, Pie Menu, Tool, etc.
- Option to import-export to-from Collections and between modes

#### 2. Pie Menu
- Smart Isolate
- Select Ungroupped
- Change Zen Sets Mode

#### 3. N-Panel
- Smart Isolate
- Select Ungroupped

#### 4. Tools
##### 4.1. Assign Materials to Object Groups
##### 4.2. Object Auto Groups:
- By Object Type
- By Object Linked Data
- By Object Material
- By Single Object in the Group
- By Custom Delimiter (any Blender or third-party Select Object Operator)
##### 4.3. Remove Objects with linked data from Groups
Makes only unique objects in groups

### Enhancement:
1. Option to change Pie Assist Font Size
2. Option to switch off Collection BoundBox
3. Option to switch off Auto Update Draw Cache

### Fix:
1. Fixed Pie Menu Smart Select renames Collections
2. Fixed Draw is not working in Blender 3.3
3. Fixed Append with Move Objects deactivated doesn't link objects

---
## Version 1.3.4
### Fix
1. Select option in Group Selector Tool

---
## Version 1.3.3
### Fix
- Blender 3.2.0 support

---
## Version 1.3.0
### New:

#### 1. UV Support for Zen Sets
##### 1.1. Display System
- Highlight Zen Sets groups in UV Editor
- Option to show groups in UV Editor in UV Non Sync mode when mesh is not selected
##### 1.2. Pie Menu
Besides standard Zen Pie Menu options to toggle hide, select, append-remove etc.:
- Convert Collection to Parent Object and back
- Pie menu assist
##### 1.3. WorkSpace Tool
- Help menu F1
- Tool Smart Select - Ctrl + Right (Clear Selection), Shift + Right (Keep active group)
- Assign to Pinned group
##### 1.4. Tools
- Assign UV Borders
- Auto Groups by Custom Operators
- Tool operations in UV Editor: Smart Select, Select Group, Invert UV Selection
##### 1.5. N-Panel
- Object Mode filter options: Selected Parents, Selected Collections, Selected Objects
- UV Operations: Select, Append, Intersect, Remove

### Enhancement:
1. Display system detect grab and drag operations
2. Indicator if Object Collection is isolated
3. Convert Collection to Parent Object with storing of Pivots by calculated collections center
4. Display Object Pivot state: Transform Origins, Locals, Parents
5. Sticky 2D label

### Fix:
1. Fixed UI List Drag indicator bug

---
## Version 1.2.0
### New:

#### 1. Functionality for the management of collections
##### 1.1. Display System
- Boundbox of the Selected Collection in the Viewport
- Highlight Objects in Collections
- Get the list of colorized Selected Objects
##### 1.2. Pie Menu
Besides standard Zen Pie Menu options to toggle hide, select, append-remove etc.:
- Duplicate collection (Linked, Instanced)
- Exclude-include collection
##### 1.3. WorkSpace Tool
- Quick collection toolbar with the options to append-remove object, toggle hide, select, exclude, disable
- Mouse operations to isolate, unhide, invert object selection
##### 1.4. Tools
- Batch rename Collections
- Convert collections to nested objects and back

#### 2. Palette
- Create-delete user Palette
- Reorder the Palette colors (operators of moving up/down one position)
- Sort Colors by Hue, Saturation, Value, Luminance
- Export Group colors to the Active Palette
- Assign color from the Active Palette in sequence or random order

### Enhancement:
1. Isolate-restore functionality in eye-icon
2. Option to switch off select after unhide, isolate operations
3. Better Zen Sets tool arrangement in N-Panel Tool tab and Sidebar Tool tab
4. Removed viewport shading from Zen Sets Groups color icons, so icons now have true color

### Fix:
1. Fixed error after Auto Groups undo operation
2. Fixed performance drop if Preferences panel was expanded

---
## Version 1.1.0
### New:
1. N-Panel Toolbar:
- Display Toggle
- Selection Follows Selected Group
- Auto Frame Selected Group
- Objects Group Info toggle button
- Visibility Group Icon (eye icon) (Toggles the visibility of the Group in the 3D View)
- Selected Object Groups | All Scene Groups toggle button
2. Undo operations
3. Group transfer among modes (Vert Sets Groups to Face Maps Groups etc.) (Copy-Paste clipboard operations)
4. Help-context system (Quick operator documentation by pressing F1)
5. Option to override all overlay settings (layers opacity, point size, line width etc.)
6. Option to override Zen Sets keymaps in all modes (Edit Mode, WorkSpaceTool, Operators)
7. Option to find and select all objects in Scene that has the Group
8. Option to Batch rename Groups
9. Auto Groups delimiters: Normal, Material, Seam, Sharp, UVs

### Enhancement:
1. Improved N-Panel interface performance with huge amount of groups (100 and more)
2. Avoiding of empty Groups creation in multi-object mode (Add, Append operators)
3. Keep groups after Join Objects and Append Objects
4. Better performance of overlay draw system
5. Import-export operators have been groupped in Menu and Panel
6. Multi-object groups represention (ability to see only groups in selected objects or in all Scene)
7. Inherit only necessary groups in 'Create Objects from groups' operator instead of all Scene groups

### Fix:
1. Faces overlay Z-Fight if mesh has transformations
2. Edges overlay Z-Fight in all modes
3. Loosing of groups while switching between objects
4. Parts elements deletion after groups deletion
5. Global object cleanup to avoid undeleted group layers

---
## Version 1.0.0
- First Release!