feature
========

### 目标

提供一个http前端。

约定

```
origen -- xunlei -- server -- dev
    |<-add-|           |       |
    |      |-download->|       |
    |                  |-pull->|
    |-----origen_download----->|
```

### 已知

from lixian import XunleiClient
x = XunleiClient(name, password)

* 列表
list = x.read_all_tasks()
    * 普通任务
    list[0]['type'] != 'bt'
    list[0]['xunlei_url']
    * bt任务
    list[0]['type'] == 'bt'
    bt_files = x.list_bt(list[0])
    此时，bt_file['name']包含文件夹名称，比如
    bt_file['name'] == 'aaa/bbb/ccc.avi'

