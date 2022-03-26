# max_result_window

https://blog.csdn.net/m0_38130105/article/details/95494386


解决方法 配置索引模板

```json
{
  "index": {
    "lifecycle": {
      "name": "serilog-log"
    },
    "max_result_window": "10000000"
  }
}
```
