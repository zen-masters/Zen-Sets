# Zen Sets N-Panel
N-Panel contains all Zen Sets addon functionality and consits of Main, Tools, Preferences and Help collapsible subpanels.
> **NOTICE! This panel is available only in edit mode, when the object being edited as a mesh**

![npanel](img/screen/n_panel/n_panel_preview.gif)

---

## Main Subpanel
Contains all basic functionality for managing Zen Sets

![npanel_main](img/screen/n_panel/n_panel_main.png)

### Active Zen Sets Element Switch
Gives an option to change type of mesh geometry (vertex, edge or face) that can be assigned to a group

![npanel_elements](img/screen/elements.png)

> **NOTICE! Zen Sets active element is synchronized with the Blender mesh selection mode**

![elem_sync](img/screen/elements_sync.gif)

### Active Zen Sets Mode Switch
![Modes](img/screen/modes.png)

#### Sets mode
One element (Vertex, Edge, Face) may be assigned to more than one group and only active group is displayed in the viewport

![sets_mode](img/screen/sets_mode.gif)

#### Parts mode
One element (Vertex, Edge, Face) may belong only to one group and all groups or active group can be displayed in the viewport

![parts_mode](img/screen/parts_mode.gif)

### Groups List
![n_panel_list](img/screen/n_panel/n_panel_list.png)

Contains the following information:

- **Group Color**
- **Group Name**
- **Mesh Elements Count**
- **Objects Count**

### Selection to group
#### Append
Appends selected Elements to selected Group

![select_append](img/screen/n_panel/select_append.gif)

#### Remove
Removes selected Elements from selected Group

![select_remove](img/screen/n_panel/select_remove.gif)

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

### Display group
You can highlight the active group in [Sets mode](npanel.md#sets-mode) or all groups in [Parts mode](npanel.md#parts-mode). Also you can hide, unhide active group or hide elements that don't belong to the active group

![group_hide_unhide](img/screen/n_panel/group_hide_unhide.gif)
#### Hide
Hides active group
#### Unhide 
Unhides active group
#### Invert hide
Hides elements that don't belong to active group
#### Display
Toggles the display of the active group in [Sets Mode](npanel.md#sets-mode) or all groups in [Parts Mode](npanel.md#parts-mode)

![group_highlight](img/screen/n_panel/group_highlight.gif)

## Tools Subpanel
![tools](img/screen/n_panel/tools.png)

## [Help](help.md) Subpanel
![](img/screen/help.png)