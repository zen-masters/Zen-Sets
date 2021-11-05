# Zen Sets N-Panel
N-Panel contains all Zen Sets addon functionality and consits of Main, Tools, Preferences and Help collapsible subpanels.
> **NOTICE! This panel is available only in edit mode, when the object being edited as a mesh**

![npanel](img/screen/n_panel/n_panel_preview.gif)

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

### Selection to group
#### Append
Append selected Elements to selected Group

![select_append](img/screen/n_panel/select_append.gif)

#### Remove
Remove selected Elements from selected Group

![select_remove](img/screen/n_panel/select_remove.gif)

### Group to selection
#### Select
Select Elements of selected Group
- **Clear selection** - an option to clear previous selection

![group_select](img/screen/n_panel/group_select.gif)

#### Deselect
Remove selected Group Elements from mesh selection
![group_deselect](img/screen/n_panel/group_deselect.gif)
