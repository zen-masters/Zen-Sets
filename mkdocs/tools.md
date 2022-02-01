# Tools
![tools](img/screen/n_panel/tools.png)

## Edit Mesh Tools

### Auto Groups
![auto_groups](img/screen/tools/auto_groups.gif)

### Create Objects from Groups
![create_objects](img/screen/tools/create_objects.gif)

### Assign materials to Groups
![assign_materials](img/screen/tools/assign_materials.gif)

### Split Group edges
![split_edges](img/screen/tools/split_group_edges.gif)

### Mark and clear seams
The menu options marks or clear seams in the Selected Group
![mark_seams](img/screen/tools/mark_seams.gif)

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
