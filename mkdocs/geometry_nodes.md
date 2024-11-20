# Geometry Nodes
Every Zen Sets group can be used in Geometry Nodes. Attribute implementation depends on Sets or Parts mode

| ![](img/screen/geo_nodes/geo_nodes_preview.png) |
|---|
| |

!!! WARNING
    Do not delete or rename Group Attributes manually !
    ![](img/screen/geo_nodes/geo_nodes_parts_not_delete.png)

## Parts Mode
There is a fixed attribute for every Parts mode. Every group has its own unique integer identifier within the current Scene. 

!!! NOTE
    Value 0 is used for elements that are not assigned to any group

| Mode | Mesh Element | Attribute Name |
|---|---|---|
| Vert Parts | Vertex | zen_vert_u_hash_layer |
| Edge Parts | Edge | zen_edge_u_hash_layer |
| Face Parts | Face | zen_face_u_hash_layer |
| Face Maps | Face | face_maps |

## Sets Mode
Every group in Sets Mode is exposed as separate integer attribute with 1 value if elemement belongs to the group and 0 if not.

| ![](img/screen/geo_nodes/geo_nodes_face_attr_group.png) |
|---|
| Option to switch attribute naming |

| ![](img/screen/geo_nodes/geo_nodes_sync_attr_name.png) |
|---|
| Face Sets group and its attribute |

### Attribute Names Match Group Name
If option 'Sync Attribute Name' is set attribute will have the same name as the group name

!!! WARNING
    You should take care about group naming to prevent name collisions with Blender internal attributes

    | ![](img/screen/geo_nodes/geo_nodes_name_collisions.png) |
    |---|
    | Example of attribute name collisions |

### Attribute Names Are Unique
If option 'Sync Attribute Name' is unset then attribute will have unique name with the next format:
```
zen_{vert|edge|face}_{128-bit uuid}
```

| ![](img/screen/geo_nodes/geo_nodes_sets_mode.png) |
|---|
| Example of the default Face Set attribute |

### How To Change Face Sets Attribute Name
| ![](img/screen/geo_nodes/geo_nodes_change_name_res.png) |
|---|
| Example of Face Sets group renamed to the simple name |

1. Call **Change Group Attribute Name** operator
![](img/screen/geo_nodes/geo_nodes_sets_change_name.png)

2. Type New Attribute Name and press **OK**
![](img/screen/geo_nodes/geo_nodes_sets_change_name_2.png)

## Create Node

!!! NOTE
    Available in Parts Mode only

### Value To Color Node
| ![](img/screen/geo_nodes/geo_nodes_value_to_color.png) |
|---|
| Add node to the editor and connect to outputs |
| ![](img/screen/geo_nodes/add_color_node.gif) |
| Encode group identifiers with color values and create temporary color attribute |
| ![](img/screen/geo_nodes/add_color_node_shading.gif) |

### Selection By ID Node
| ![](img/screen/geo_nodes/select_by_id.gif) |
|---|
| Example how to add and use Select By ID node for Extrude Mesh modificator |

### Group Name To ID
| ![](img/screen/geo_nodes/group_name_to_id.gif) |
|---|
| Example how to use group names in Geometry Nodes |
