## Q: 有办法把方法挂载到this上面吗？挂到vue实例上，全局那种，到每个组件都能直接this.xxx()调用。

如图![](https://i.loli.net/2018/11/21/5bf4f8a857021.png)

每个页面使用的时候直接 this.$test

## Q: ios 老版本升级（包名修改的那个版本）出现的问题解决方案
基础包名改版版本日志： https://bmfe.github.io/eros-docs/#/zh-cn/update_log_all?id=_20181011
>  问题1 如图

解决方案：若出现该位置报错，改为图中划线的代码即可

![](https://i.loli.net/2018/11/21/5bf4f8e4c8671.png)




> 问题2 如图
![](https://i.loli.net/2018/11/21/5bf4f9244e907.png)
若出现如上图报错的

解决方案：搜索BMBaseLibrary，这两处地方将其改为 ErosPluginBaseLibrary。然后重新run即可

如图
![](https://i.loli.net/2018/11/21/5bf4f924ae23a.png)


## Q: android 提交google play收到SSL Error Handler错误

因为 SSL 的验证 google 检查的更严一些，但是国内一般都不会做这个检测。

https://www.cnblogs.com/shoneworn/p/8182615.html

你可以参考这个 对 com.benmu.framework.activity.GlobalWebViewActivity 类 做一些修改吧。

> 在 GlobalWebViewActivity 120行代码开始修改成如下。

``` java
     @Override
        public void onReceivedSslError(WebView view, SslErrorHandler handler, SslError error) {
//            handler.proceed();
            final SslErrorHandler mHandler;
            mHandler = handler;
            AlertDialog.Builder builder = new AlertDialog.Builder(activity);
            builder.setMessage("ssl证书验证失败");
            builder.setPositiveButton("继续", new DialogInterface.OnClickListener() {
                @Override
                public void onClick(DialogInterface dialog, int which) {
                    mHandler.proceed();
                }
            });
            builder.setNegativeButton("取消", new DialogInterface.OnClickListener() {
                @Override
                public void onClick(DialogInterface dialog, int which) {
                    mHandler.cancel();
                }
            });
            builder.setOnKeyListener(new DialogInterface.OnKeyListener() {
                @Override
                public boolean onKey(DialogInterface dialog, int keyCode, KeyEvent event) {
                    if (event.getAction() == KeyEvent.ACTION_UP && keyCode == KeyEvent.KEYCODE_BACK) {
                        mHandler.cancel();
                        dialog.dismiss();
                        return true;
                    }
                    return false;
                }
            });
            AlertDialog dialog = builder.create();
            dialog.show();
        }
```
> 代码如果报错可能是因为你没有导包导致的，请对应impor 对应的包。

    <bmchart scr='bmlocal://assets/heatmap/bm-chart.html' ref="chart" :options="$format(bmapInfo)" style="width:750; height:520;"  @finish='finish'></bmchart>
