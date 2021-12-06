# Changelog

---
## 1.1.0
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
## 1.0.0
- First Release!