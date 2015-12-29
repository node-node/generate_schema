
# JSON Object to JSON Schema for browser

# Usage
    
   ```
   <script src="generate_schema/json.js"></script>
<script src="generate_schema/type-of-is.js"></script>

    var json = {
    "Array": [1, 2, 3],
    "Boolean": true,
    "Null": null,
    "Number": 123,
    "Object": {"a": "b", "c": "d"},
    "String": "Hello World"
};


var generateSchema = new GenerateSchema(json);
var json_str = JSON.stringify(generateSchema);
console.log(json_str);
```

# Output
    ```
    {"type":"object","properties":{"Array":{"type":"array","items":{"type":"number"}},"Boolean":{"type":"boolean"},"Null":{"type":"null"},"Number":{"type":"number"},"Object":{"type":"object","properties":{"a":{"type":"string"},"c":{"type":"string"}}},"String":{"type":"string"}}}
    ```

