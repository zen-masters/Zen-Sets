# Tools
![tools](img/screen/n_panel/tools.png)

## Edit Mesh Tools

### Auto Groups
![auto_groups](img/screen/tools/auto_groups.gif)

### Auto Groups by custom operator
![auto_custom](img/screen/tools/auto_groups_with_custom.gif)

### Create Objects from Groups
![create_objects](img/screen/tools/create_objects.gif)

### Assign materials to Groups
![assign_materials](img/screen/tools/assign_materials.gif)

### Split Group edges
![split_edges](img/screen/tools/split_group_edges.gif)

### Mark and clear seams
The menu options marks or clear seams in the Selected Group
![mark_seams](img/screen/tools/mark_seams.gif)

### Assign to Pinned Group
!!! Notice
    **This option is available only in Sets Mode**

![to_pinned](img/screen/tools/assign_to_pinned.gif)

### Assign UV Borders To Group
!!! Notice
    **This option is available only in Edge Sets Mode**

![to_uv_borders](img/screen/tools/assign_uv_borders.gif)

### Remove Weight
[](#change-weight-in-selected-group)

### Change Weight in Selected Group

## Object Tools

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
![convert_parent_object_to_collection](img/screen/tools/convert_parent_object_to_collection.gif)

### Convert Collection to Parent Object
![convert_collection_to_parent_object](img/screen/tools/convert_collection_to_parent_object.gif)

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

| ![sort_collections](img/screen/collections/sort_collections_2.gif) |
|---|
| Sort Children Collections demo |

### Remove Linked
| ![remove_linked](img/screen/collections/remove_linked.gif) |
|---|
| Remove Objects with linked data from Group |

### Set Sculpt Mask
| ![set_mask_settings](img/screen/tools/set_sculpt_mask_settings.png) |
|---|
| Set Sculpt Mask settings |

| ![set_mask_settings](img/screen/tools/set_sculpt_mask.gif) |
|---|
| Set Sculpt Mask Demo |
