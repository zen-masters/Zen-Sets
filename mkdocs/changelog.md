# Changelog

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