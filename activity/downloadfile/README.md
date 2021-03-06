# Download File

Download a file

## Installation

```bash
flogo install github.com/retgits/flogo-components/activity/downloadfile
```
Link for flogo web:
```
https://github.com/retgits/flogo-components/activity/downloadfile
```

## Schema
Inputs and Outputs:

```json
{
"inputs": [
        {
            "name": "url",
            "type": "string",
            "required": true
        },
        {
            "name": "writeToDisk",
            "type": "bool",
            "required": true
        },
        {
            "name": "filename",
            "type": "string"
        },
        {
            "name": "append",
            "type": "bool"
        },
        {
            "name": "create",
            "type": "bool"
        }
    ],
    "outputs": [
        {
            "name": "result",
            "type": "string"
        }
    ]
}
```
## Inputs
| Input       | Description                                                                                                   |
|:------------|:--------------------------------------------------------------------------------------------------------------|
| url         | The full URL of the file you want to download                                                                 |
| writeToDisk | Write the downloaded file to disk (if set to true, the `filename`, `append`, and `create` need to be set too) |
| filename    | The name of the file you want to write to (like `data.txt` or `./tmp/data.txt`)                               |
| append      | Append to the file or overwrite existing content (setting this to false deletes and recreates the file)       |
| create      | Create the file if it doesn't exist                                                                           |

## Ouputs
| Output      | Description                                                        |
|:------------|:-------------------------------------------------------------------|
| result      | The result (either `OK` or the error that was generated by the OS) |