# Zen Sets API
We offer to use our API for addon creators and other users to highlight differents parts of Mesh elements (verts, edges, faces) or UV loops

!!! example "ZenSets/API/example_create_groups.py"
	![api_example](img/screen/api/api_create_groups.gif)

    ??? note "Source Code"
        ``` py
        import bpy
        import bmesh
        
        
        class DemoNames:
        group_even = 'Example - Even'
        group_odd = 'Example - Odd'
        
        
        def api_demo_create_groups():
        
        C = bpy.context
        
        if C.mode != 'OBJECT':
        	bpy.ops.object.mode_set(mode='OBJECT')
        
        bpy.ops.mesh.primitive_cube_add(enter_editmode=True, location=(-4, 0, 0))
        
        p_obj = C.active_object
        
        p_scene = C.scene
        # set 'Face Parts' mode
        p_scene.zen_sets_active_mode = 'face_u'
        
        # create 1 group with object even faces (0, 2, 4 ...)
        bm = bmesh.from_edit_mesh(p_obj.data)
        for face in bm.faces:
        	face.select_set(face.index % 2 == 0)
        
        bpy.ops.zsts.assign_to_group(
        	group_name=DemoNames.group_even, group_color=(1, 0, 0))
        
        # create 2 group with object odd faces (1, 3, 5 ...)
        bm = bmesh.from_edit_mesh(p_obj.data)
        for face in bm.faces:
        	face.select_set(face.index % 2 != 0)
        
        bpy.ops.zsts.assign_to_group(
        	group_name=DemoNames.group_odd, group_color=(0, 0, 1))
        
        
        # DEMO
        api_demo_create_groups()
        ```

## Scene Properties

<dl class="py class">
	<dt class="sig sig-object py" id="zen_sets_active_mode">
		<em class="property"><span class="pre">enum</span></em>
		<span class="sig-prename descclassname"><span class="pre">bpy.types.Scene.zen_sets_active_mode</span></span>
		<a class="headerlink" href="#zen_sets_active_mode" title="Permalink link"></a>
	</dt>
</dl>

> * `vert` - Vertex Sets
> * `vert_u` - Vertex Parts
> * `edge` - Edge Sets
> * `edge_u` - Edge Parts
> * `face` - Face Sets
> * `face_u` - Face Parts
>> **Type:** enum in {`vert`, `vert_u`, `edge`, `edge_u`, `face`, `face_u`}

## Operators

<dl class="py class">
	<dt class="sig sig-object py" id="zsts.assign_to_group">
		<!-- <em class="property"><span class="pre">operator</span></em> -->
		<span class="sig-prename descclassname"><span class="pre">bpy.ops.</span></span>
		<span class="sig-name descname"><span class="pre">zsts.assign_to_group</span></span>
		<span class="sig-paren">(</span>
		<em class="sig-param"><span class="n"><span class="pre">identifier=""</span></span></em>, 
		<em class="sig-param"><span class="n"><span class="pre">group_name=""</span></span></em>, 
		<em class="sig-param"><span class="n"><span class="pre">group_color=(0, 0, 0)</span></span></em>, 
        <em class="sig-param"><span class="n"><span class="pre">group_indices=[]</span></span></em>, 
        <em class="sig-param"><span class="n"><span class="pre">group_mode='SELECTED'</span></span></em> 
		<span class="sig-paren">)</span>
		<a class="headerlink" href="#zsts.assign_to_group" title="Permalink link"></a>
	</dt>
</dl>

> Assign Mesh Elements (Verts, Edges, Faces) to Group, deleting any existing assignments

> **Parameters:**

>>> * **identifier** (_str_, (_optional_)) - Unique identifier of the Group.
>>> * **group_name** (_str_, (_optional_)) - Group Name.
>>> * **group_color** (_Color_, (_optional_)) - Group Color.
>>> * **group_indices** (_Collection_, (_optional_)) - Collection of Group Indices.
>>> * **group_mode** (_enum_ in _{'SELECTED', 'INDICES'}_, (_optional_)) - Assign Group Mode.


>>>	``` py
	import bpy
	# create 1 group with object even faces (0, 2, 4 ...)
	bpy.ops.zsts.assign_to_group(
		group_mode='INDICES',
		group_indices=tuple(
			{'item': face.index, 'name': p_obj.name}
			for face in bm.faces if face.index % 2 == 0),
		group_name='Example - Even', group_color=(1, 0, 0))
	```
