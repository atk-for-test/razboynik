#API SPECIFICATIONS

##URL
- [POST] `http://localhost:{port}/api/shell`
- [POST] `http://localhost:{port}/api/php`

##Shell
Post data type: `JSON`

Required parameters:
- `[config][url]` (string)
- `[request][cmd]` (string)

Optional parameters:
- `[config][parameter]` (string) (default: "razboynik")
- `[config][method]` (string) ["GET", "POST", "HEADER", "COOKIE"] (default: "GET")
- `[config][key]` (string) (default: "FromRussiaWithLove<3")
- `[config][raw]` (boolean) (default: false)
- `[request][scope]` (string) (default: "")
- `[request][method]` (int) [0 => "system()", 1 => "shell_exec()"] (default: 0)

Example:
```json
{
    "config": {
        "url": "http://target.com/script.php",
        "method": "POST",
        "raw": false
    },
    "request": {
        "cmd": "ls",
        "method": 1
    }
}
```

##PHP