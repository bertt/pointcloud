# I3S point cloud scene layer: defaultGeometrySchema

Attribute description as field.

### Related:

[pointcloud::store](store.md)
### Properties

| Property | Type | Description |
| --- | --- | --- |
| **geometryType** | string | The type of primitive. Only points are supported for point cloud scene layer.<div>Possible values are:<ul><li>`points`</li></ul></div> |
| header | [] | The header in binary buffers. Currently not supported for point cloud scene layer. |
| **topology** | string | This property is currently IGNORED for point cloud scene layer since it only conatains geometry position and not the vertex attributes.<div>Possible values are:<ul><li>`PerAttributeArray`</li></ul></div> |
| **encoding** | string | Only 'lepcc-xyz' compression is currently supported.<div>Possible values are:<ul><li>`lepcc-xyz`</li></ul></div> |
| ordering | string[] | Currently the geometry contains XYZ only, so vertex attribute must only list 'position'.<div>Possible values for each array string:<ul><li>`position`: vertex coordinates</li></ul></div> |
| **vertexAttributes** | [pointcloud::vertexAttributes](vertexAttributes.md) | The vertex buffer description. |

*Note: properties in **bold** are required*

### Examples 

#### Example: defaultGeometrySchema 

```json
 {
  "defaultGeometrySchema": {
    "geometryType": "points",
    "header": [],
    "topology": "PerAttributeArray",
    "encoding": "lepcc-xyz",
    "vertexAttributes": {
      "position": {
        "valueType": "Float64",
        "valuesPerElement": 3
      }
    },
    "ordering": [
      "position"
    ]
  }
} 
````

