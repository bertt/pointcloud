# I3S point cloud scene layer: Values

A scalar or vector value.

### Related:

[pointcloud::attributeInfo](attributeInfo.md), [pointcloud::vertexAttributes](vertexAttributes.md)
### Properties

| Property | Type | Description |
| --- | --- | --- |
| **valueType** | string | Type of the attribute values after decompression, if applicable. Please note that `string` is not supported for point cloud scene layer attributes.<div>Possible values are:<ul><li>`Int8`</li><li>`UInt8`</li><li>`Int16`</li><li>`UInt16`</li><li>`Int32`</li><li>`UInt32`</li><li>`Float`</li><li>`Double`</li></ul></div> |
| **valuesPerElement** | number | Number of components. |

*Note: properties in **bold** are required*

### Examples 

#### Example: Scalar value definition 

```json
 {
  "attributeValues": {
    "valueType": "UInt16",
    "valuesPerElement": 1
  }
} 
````

#### Example: Vector value definition 

```json
 {
  "attributeValues": {
    "valueType": "UInt8",
    "valuesPerElement": 3
  }
} 
````

