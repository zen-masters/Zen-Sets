# Tools
Zen Sets provides a variety of tools for editing meshes and organizing objects in Blender. Tools can be accessed either or from N-Panel popup menu

| ![tools](img/screen/n_panel/tools.png) | ![tools_intro](img/screen/tools/tools_intro.png) |
|---|---|
| Tools Subpanel | N-Panel Popup menu |

## Edit Mesh Tools

### Auto Groups
| ![auto_groups](img/screen/tools/auto_groups.gif) |
|---|

### Auto Groups by custom operator
| ![auto_custom](img/screen/tools/auto_groups_with_custom.gif) |
|---|

### Create Objects from Groups
| ![create_objects](img/screen/tools/create_objects.gif) |
|---|

### Assign materials to Groups
| ![assign_materials](img/screen/tools/assign_materials.gif) |
|---|

### Split Group edges
| ![split_edges](img/screen/tools/split_group_edges.gif) |
|---|

### Mark and clear seams
The menu options marks or clear seams in the Selected Group

| ![mark_seams](img/screen/tools/mark_seams.gif) |
|---|

### Assign to Pinned Group
!!! Notice
    **This option is available only in Sets Mode**

![to_pinned](img/screen/tools/assign_to_pinned.gif)

### Assign UV Borders To Group
!!! Notice
    **This option is available only in Edge Sets Mode**

| ![to_uv_borders](img/screen/tools/assign_uv_borders.gif) |
|---|
| Assign UV Borders demo |

### Remove Weight
Remove elements with Vertex Weight in given range from Active or All Group(s)

!!! tip
    This operator can be used to remove Elements with Zero Weight from Group

| ![rem_w](img/screen/tools/remove_weight_settings.png) |
|---|
| Remove Weight settings |

| ![rem_w_demo](img/screen/tools/remove_weight_demo.gif) |
|---|
| Remove Weight settings demo |

### Change Weight in Selected Group
| ![change_w](img/screen/tools/change_weight.gif) |
|---|

### Set Sculpt Mask
| ![set_mask_settings](img/screen/tools/set_sculpt_mask_settings.png) |
|---|
| Set Sculpt Mask settings |

| ![set_mask_settings](img/screen/tools/set_mask_demo.gif) |
|---|
| Set Sculpt Mask Demo |

## Object Tools

### Rename Group
It is available to rename Group (Collection) from several places

| ![rename_group](img/screen/tools/rename_group.png) |
|---|
| 1. Rename active group in Zen Sets toolbar |

| ![rename_group_pie](img/screen/tools/rename_group_pie.png) |
|---|
| 2. Rename active group in Pie Menu |

| ![rename_group_smart](img/screen/tools/rename_group_smart.png) |
|---|
| 3. Rename active group in tweak panel of Smart Select operator |

### Batch Rename Groups
![batch](img/screen/tools/batch_rename_groups.gif)

### Duplicate Collection
This will create a visually-identical copy of the Active Collection object(s).

This copy are new objects, which share data-blocks with the original objects (by default, all the materials, textures, and F-curves), but which has copied others, like the mesh, for example. That is why this form of duplication is sometimes called **shallow link**, because not all data-blocks are shared; some of them are **hard copied**!

![object_duplicate_collection](img/screen/tools/object_duplicate_collection.gif)

### Duplicate Collection Linked
You also have the choice of creating a Linked Duplicate rather than a Duplicate; this is called a **deep link**.

This will create a new object with all of its data linked to the original object. If you modify one of the linked objects in Edit Mode, all linked copies are modified. Transform properties (object data-blocks) still remain copies, not links, so you still can rotate, scale, and move freely without affecting the other copies.

![object_duplicate_linked_collection](img/screen/tools/object_duplicate_linked_collection.gif)

### Duplicate as Instance
This creates an instance of the collection with the transformation of the object. Collection instancers can be animated using actions, or can get a Proxy.

![object_duplicate_instanced_collection](img/screen/tools/object_duplicate_instanced_collection.gif)

### Convert Parent Object to Collection

| ![par_to_col_settings](img/screen/collections/parent_object_to_collection_settings.png) |
|---|
| Convert Parent Object to Collection settings |

- **Skip Empty Objects**
    * **Auto** - Skip Empty Parent Objects by calculated Collection Center
    * **Skip All** - Skip all Empty Parent Objects
    * **Load All** - Load all Empty Parent Objects
- **Default Position**
    * **Zero Point** - Move Parent object to zero coordinate position
    * **Cursor 3D** - Move Parent object to Cursor 3D position
- **Calculate Center**
    * **By Default Position** - Collection Center will be defined by Default Position Zero Point or Cursor 3D
    * **By Objects** - Collection Center will be calculated as average children origins point
    * **By Nested Objects** - Collection Center will be calculated as average itself children and all nested collections children origins point
- **Use Average Rotation** - Calculate Center position with average rotation
- **Use Average Scale** - Calculate Center position with average scale

| ![convert_parent_object_to_collection](img/screen/tools/convert_to_collection.gif) |
|---|
| Convert Parent Object to Collection demo |

### Convert Collection to Parent Object

| ![col_to_par_settings](img/screen/collections/collection_to_parent_object_settings.png) |
|---|

- **Default Position**
    * **Zero Point** - Move Parent object to zero coordinate position
    * **Cursor 3D** - Move Parent object to Cursor 3D position
- **Calculate Center**
    * **By Default Position** - Collection Center will be defined by Default Position Zero Point or Cursor 3D
    * **By Objects** - Collection Center will be calculated as average children origins point
    * **By Nested Objects** - Collection Center will be calculated as average itself children and all nested collections children origins point
- **Use Average Rotation** - Calculate Center position with average rotation
- **Use Average Scale** - Calculate Center position with average scale
- **Select All** - Select all child Objects
- **Display As** - Representation of Parent Object as value of enum ['Plain Axes', 'Arrows', 'Single Arrow', 'Circle', 'Cube', 'Sphere', 'Cone', 'Image']

| ![convert_collection_to_parent_object](img/screen/tools/convert_to_parent_object_2.gif) |
|---|
| Convert Collection to Parent Object demo |

### Example How To Rotate Collection Around a Point

| ![how_to_rotate](img/screen/tools/how_to_rotate_collection_by_axis.gif) |
|---|

### Sort Collections
Blender Outliner has only creation order in the list of collections. There is an option "sort alphabetically" but it only works for objects. For those who has numerious collections we offer "Sort Collection Children" option

| ![sort_tweak](img/screen/collections/sort_collections_tweak.png) |
|---|
| Sort Collections settings |

#### Modes
- **Human Sort** - the ordering of strings in alphabetical order, except that multi-digit numbers are treated atomically, i.e., as if they were a single character
- **Human Last Integer** - sort by last integer, than in alphabetical order
- **Human First Integer** - sort by first integer, than in alphabetical order
- **Alpha Sort** - Pure alphabetical sort order
- **Shuffle** - Shuffle a list (reorganize the order of the Collection items)

| ![sort_shuffle](img/screen/collections/sort_shuffle.png) | ![sort_shuffle](img/screen/collections/sort_human.png) |
|---|---|
| ![sort_shuffle](img/screen/collections/sort_shuffle.png) | ![sort_alpha](img/screen/collections/sort_alpha.png) |

#### Order of sort
##### 1. Suffix (Delimiter string)
If suffix value is set, then Collections with suffix go up

| Full name | Suffix | Suffix substring |
|---|---|---|
| Collection.001 | . | 001 |
| Collection.002 | . | 002 |

| ![sort_suffix](img/screen/collections/sort_suffix.png) |
|---|
| Example: **sort by suffix '.'** |

##### 2. Prefix (Delimiter string)
If prefix value is set, then Collections with prefix go up

| Full name | Prefix | Prefix substring |
|---|---|---|
| HerCollection.001 | Collection | Her |
| HisCollection.001 | Collection | His |

| ![sort_prefix](img/screen/collections/sort_prefix.png) |
|---|
| Example: **sort by prefix '.'** |

##### 3. Body Substring from suffix to prefix
If prefix is set, then substring starts from prefix otherwise from the beginning

If suffix is set, then substring ends till suffix otherwise the end

| Full name | Prefix | Suffix | Body Substring |
|---|---|---|---|
| start-Collection001.end  | - | . | Collection001 |
| start-Collection002.end  | - | . | Collection002 |
| start-Collection003.end  | - | . | Collection003 |

| ![sort_collections](img/screen/collections/sort_collections_2.gif) |
|---|
| Sort Children Collections demo |

### Remove Linked
| ![remove_linked](img/screen/collections/remove_linked.gif) |
|---|
| Remove Objects with linked data from Group |

### Join Objects
Gives an option to mark all mesh in object with vert, face part or face map group before Blender standard [Join](https://docs.blender.org/manual/en/latest/scene_layout/object/editing/join.html) operation. Thus it will be available to split them back into objects or to no in newly created mesh where is each previous object mesh part now

| ![join_object](img/screen/collections/join_objects.gif) |
|---|
| Join objects in group(s) and optionally mark them as face parts |

| ![join_objects_uv](img/screen/tools/join_object_detect_uvs.gif) |
|---|
| Example how to detect UV Maps with the same name when objects were joined |
