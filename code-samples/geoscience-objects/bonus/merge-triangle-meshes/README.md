# Merge Triangle Meshes
This folder contains a Jupyter notebook showing how to select any number of existing triangle mesh objects from an Evo workspace using checkboxes, merge them into a single mesh, and publish the result as a new triangle mesh object.

## Inputs
Two or more [triangle mesh](https://developer.seequent.com/docs/data-structures/geoscience-objects/schemas/objects/triangle-mesh/) objects in the selected Evo workspace. The notebook lists every triangle mesh in the workspace and you tick the ones to merge.

All selected meshes must use the same coordinate reference system, as the notebook does not reproject data. A mesh with an unspecified coordinate reference system cannot be merged with a mesh that has one.

## Outputs
- A new triangle mesh object with the name and path you provide, containing the vertices and triangles of all selected meshes. The triangle indices of each mesh are offset by the total number of vertices in the meshes before it.

Only the mesh geometry is merged. Attributes, parts, and edges of the source meshes are not carried over.
