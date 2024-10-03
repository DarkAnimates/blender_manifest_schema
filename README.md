# Blender Manifest Schema

A JSON Schema that allows verification and autocompletion of the Blender Addon Manifest Schema inside of
Code editors, for example with the [Even Better TOML](https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml) extension in VS Code.

The URL for the JSON schema is

```
https://extensions.blender-defender.com/api/blender_manifest_v1.schema.json
```

It allows specifying two URL parameters for more control over the autocompletion/verification:

| name                  | description                                                                                                                         | default        |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| default_author        | The default autocompletion for the maintainer name                                                                                  | _empty string_ |
| additional_properties | Allow adding additional properties that aren't part of Blenders default manifest schema. `true` if present in the URL, else `false` | false          |

**Configuration of Even Better TOML**

```json
"evenBetterToml.schema.associations": {
    "blender_manifest.toml": "https://extensions.blender-defender.com/api/blender_manifest_v1.schema.json",
},
```
