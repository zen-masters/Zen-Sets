# Zen Sets N-Panel
N-Panel contains all Zen Sets addon functionality and consits of [Main](#main-subpanel), [Import-Export](imp_exp.md), [Tools](tools.md), [Preferences](preferences.md) and [Help](help.md) collapsible subpanels.

!!! Notice
    **This panel is available only in Blender Edit Mode and Object Mode**

![npanel](img/screen/n_panel/n_panel_preview.gif)    

---

## Main Subpanel
Contains all basic functionality for managing Zen Sets

![npanel_main](img/screen/n_panel/n_panel_main.png)

### Active Zen Sets Element Switch
Gives an option to change type of mesh geometry (vertex, edge or face) that can be assigned to a group

![npanel_elements](img/screen/elements.png)

!!! Notice
    **Zen Sets active element is synchronized with the Blender mesh selection mode by default**
    ![elem_sync](img/screen/elements_sync.gif)

!!! Notice
    **You can disable synchronization with mesh selection in addon preferences**
    ![sync_with_mesh_select](img/screen/preferences/sync_with_mesh_select.png)

### Active Zen Sets Mode Switch
![Modes](img/screen/modes.png)

#### Sets mode
One element (Vertex, Edge, Face) may be assigned to more than one group and only active group is displayed in the viewport

![sets_mode](img/screen/sets_mode.gif)

#### Parts mode
One element (Vertex, Edge, Face) may belong only to one group and all groups or active group can be displayed in the viewport

![parts_mode](img/screen/parts_mode.gif)

---

### Groups List
![n_panel_list](img/screen/n_panel/n_panel_list.png)

Contains the following information:

- **Group Color**
- **Group Name**
- **Mesh Elements Count**
Shows how many mesh elements (verts, edges or faces) are in the current group
- **Objects Count**
Shows how many objects in edit mode has elements with the same group
- **Visibility Group Icon (eye icon)**
    - Group is completely visible
        - ![n_panel_list_visible_icon](img/screen/n_panel/n_panel_list_visible_icon.png)
    - Group is partially visible
        - ![n_panel_list_partially_visible_icon](img/screen/n_panel/n_panel_list_partially_visible_icon.png)
    - Group is completely hidden
        - ![n_panel_list_hidden_icon](img/screen/n_panel/n_panel_list_hidden_icon.png)

---

### Toolbar
![n_panel_toolbar](img/screen/n_panel/n_panel_toolbar.png)

The Toolbar shows [Groups List](#groups-list) main settings and [Display toggle button](#display)

![n_panel_toolbar_animation](img/screen/n_panel/n_panel_toolbar_animation.gif)

- ![n_panel_toolbar_overlay](img/screen/n_panel/n_panel_toolbar_overlay.png) **Display Groups in Viewport**

- ![n_panel_toolbar_single_select](img/screen/n_panel/n_panel_toolbar_single_select.png) **Selection follows Selected Group** (Select all elements after Selected Group has been changed)

- ![n_panel_toolbar_auto_frame](img/screen/n_panel/n_panel_toolbar_auto_frame.png) **Auto Frame Selected Elements** (Move the view to the Selected elements center when selection changes)

- ![n_panel_toolbar_objects_info](img/screen/n_panel/n_panel_toolbar_objects_info.png) **Display count of objects that have the Group**

- ![n_panel_list_visible_icon](img/screen/n_panel/n_panel_toolbar_visibility_info.png) **Display hidden Groups Info**

- ![n_panel_toolbar_display_all_scene_groups](img/screen/n_panel/n_panel_toolbar_display_all_scene_groups.png) **Display all scene Groups or selected object groups**

---

### Sidebar
![sidebar](img/screen/n_panel/sidebar.png)
#### Add New Group
Creates new Group from selected mesh elements
#### Delete Active Group
Deletes Active Group from the selected Objects
#### Show Popup menu
Shows main panel Popup menu
#### Move Active Group Up
Moves active Group up in the Group List
#### Move Active Group Down
Moves active Group down in the Group List
#### Delete Groups
- **Empty Groups**
Deletes Groups that does not contain any mesh elements
- **Delete All Groups**
    * Deletes all groups in the Scene if **Display all scene Groups** option **is set**
    * Deletes all groups in the Selected Objects if **Display all scene Groups** option **is unset**

---

### Main panel Popup Menu
![popup](img/screen/n_panel/popup.png)
#### Select all objects by Group ID
Selects and adds to the Edit Mode all Objects that has the Active Group elements

![n_panel_select_all_objects](img/screen/n_panel/n_panel_select_all_objects.gif)
#### Batch rename Groups
Option to rename all Groups in the list

![copy_paste_rename](img/screen/n_panel/copy_paste_rename.gif)

---

### Selection to group
#### Append
Appends selected Elements to selected Group

![select_append](img/screen/n_panel/select_append.gif)

#### Remove
Removes selected Elements from selected Group

![select_remove](img/screen/n_panel/select_remove.gif)

---

### Group to selection
#### Select
Selects Elements of selected Group
- **Clear selection** - an option to clear previous selection

![group_select](img/screen/n_panel/group_select.gif)

#### Deselect
Removes selected Group Elements from mesh selection

![group_deselect](img/screen/n_panel/group_deselect.gif)

#### Intersect
Selects Group Elements intersected with mesh selection

![group_intersect](img/screen/n_panel/group_intersect.gif)

#### Smart select
Depends on selected mesh elements and has the next behaviour:

- **Select Group by selected Elements in Viewport**
If mesh selection belongs to Zen Sets group, all group elements are selected and other elements are deselected

- **Deselect Active Group and select Elements that does not belong to any group**
If mesh selection does not belong to any Zen Sets group, the active group is deselected and all mesh elements that don't have group metainformation are selected

![smart_select](img/screen/n_panel/group_smart_select.gif)

---

### Display group
You can highlight the active group in [Sets mode](npanel.md#sets-mode) or all groups in [Parts mode](npanel.md#parts-mode). Also you can hide, unhide active group or hide elements that don't belong to the active group

![group_hide_unhide](img/screen/n_panel/group_highlight.gif)
#### Hide
Hides active group
#### Unhide 
Unhides active group
#### Isolate
Hides elements that don't belong to active group or restore (unhide) all elements if the group was previously isolated
#### Display
Toggles the display of the active group in [Sets Mode](npanel.md#sets-mode) or all groups in [Parts Mode](npanel.md#parts-mode)

### Palette Panel
Gives an option to adjust user colors when a new color is generated for new group

![pal_auto](img/screen/n_panel/palette/pal_auto.png)
#### Auto Mode
Colors are created in random order of Zen Sets default palette

#### User Palette Mode
Colors are selected from user palette

- **Sequence Mode**
- **Random Mode**

![pal_user](img/screen/n_panel/palette/pal_user.png)


---

## [Import-Export Subpanel](imp_exp.md)
![imp_exp](img/screen/n_panel/n_panel_imp_exp.png)

## [Tools Subpanel](tools.md)
![tools](img/screen/n_panel/tools.png)

## [Help Subpanel](help.md)
![help](img/screen/help.png)