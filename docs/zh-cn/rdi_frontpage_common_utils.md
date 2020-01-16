## UI相关操作

RDIFramework.UI命名空间常用JS方法(rdiframework-ui.js)。

| 名称                                  | 说明                                           |
| ------------------------------------- | ---------------------------------------------- |
| RDIFramework.UI.saveForm              | 保存界面数据                                   |
| RDIFramework.UI.setForm               | 绑定界面控件                                   |
| RDIFramework.UI.removeForm            | 删除数据                                       |
| RDIFramework.UI.confirmAjax           | ajax询问操作                                   |
| RDIFramework.UI.existField            | 指定数据是否已经存在                           |
| RDIFramework.UI.serializeFormJson     | 序列化表单数据                                 |
| RDIFramework.UI.SetExportExcel        | Jqgrid导出Excel，将表格数据取出来，再导出Excel |
| RDIFramework.UI.DownloadExcelTemplate | 根据业务类型下载导入数据的模版文件             |
| RDIFramework.UI.ImportExcelTemplate   | 根据业务类型导入数据                           |
|                                       |                                                |

## Layer弹窗相关操作

RDIFramework.Layer命名空间常用JS方法(rdiframework-ui.js)。

| 名称                             | 说明                                             |
| -------------------------------- | ------------------------------------------------ |
| RDIFramework.Layer.layerConfirm  | 询问提示                                         |
| RDIFramework.Layer.layerForm     | 使用频率最高的自定义表单弹层（如：新增、修改时） |
| RDIFramework.Layer.layerClose    | 关闭表单弹层                                     |
| RDIFramework.Layer.prompt        | 弹出提示                                         |
| RDIFramework.Layer.close         | 关闭弹出的layer弹窗                              |
| RDIFramework.Layer.dialogOpen    | 兼容3.5以前版本自定义表单弹层                    |
| RDIFramework.Layer.dialogContent | 通过指定html内容来自定义表单弹层                 |
| RDIFramework.Layer.dialogAlert   | 自定义警告提示                                   |
| RDIFramework.Layer.dialogConfirm | 自定义确认否提示（类似javascript的confirm）      |
| RDIFramework.Layer.dialogMsg     | 常规提示内容                                     |
| RDIFramework.Layer.dialogClose   | 关闭表单弹层                                     |

## Util常用工具类相关操作

RDIFramework.Util命名空间常用JS方法(rdiframework-ui.js)。

| 名称                             | 说明                                                   |
| -------------------------------- | ------------------------------------------------------ |
| RDIFramework.Util.log            | 询问提示                                               |
| RDIFramework.Util.storage        | 本地缓存设置                                           |
| RDIFramework.Util.newGuid        | 得到guid                                               |
| RDIFramework.Util.loading        | 加载提示                                               |
| RDIFramework.Util.reload         | 重新加载当前窗口                                       |
| RDIFramework.Util.loadStyles     | 动态加载css文件                                        |
| RDIFramework.Util.iframe         | 获取指定iframe窗口                                     |
| RDIFramework.Util.currentIframe  | 得到当前iframe                                         |
| RDIFramework.Util.changeUrlParam | 改变url参数值                                          |
| RDIFramework.Util.countFileSize  | 文件大小转字节、KB、MB、GB                             |
| RDIFramework.Util.arrayCopy      | 数组复制                                               |
| RDIFramework.Util.alert          | toastr提示消息栏（一般显示在屏幕中上方）               |
| RDIFramework.Util.download       | 下载文件                                               |
| RDIFramework.Util.checkedArray   | 检查是否为数组类型                                     |
| RDIFramework.Util.checkedRow     | 检查指定值是否存在（一般多用于删除、修改时是否选中行） |
| RDIFramework.Util.isExistImg     | 判断图片是否存在                                       |
| RDIFramework.Util.numberFormat   | 数据格式化                                             |
| RDIFramework.Util.request        | 得到请求地址中的参数值（常用）                         |
| RDIFramework.Util.rootPath       | 根地址                                                 |
| RDIFramework.Util.windowWidth    | 窗体宽度                                               |
| RDIFramework.Util.windowHeight   | 窗体高度                                               |
| RDIFramework.Util.formatDate     | 日期格式化处理                                         |
| RDIFramework.Util.getBrowserName | 得到当前浏览器的名称                                   |
| RDIFramework.Util.isNullOrEmpty  | 判断指定值是否为空                                     |
| RDIFramework.Util.arrayClone     | 数组克隆                                               |
| RDIFramework.Util.loadFile       | 加载js,css文件                                         |
| RDIFramework.Util.isIE           | 判断是否为IE浏览器                                     |
| RDIFramework.Util.UUID           | 生成guid                                               |