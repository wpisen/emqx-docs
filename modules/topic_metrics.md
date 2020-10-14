# 主题监控

EMQ X 提供了主题指标统计功能，可以统计指定主题下的消息收发数量、速率等指标。

## 开启主题监控功能

通过 dashboard 页面可以开启主题监控模块

打开 [EMQ X Dashboard](http://127.0.0.1:18083/)，并登陆，点击左侧的 “模块” 选项卡，选择添加

![image-20200927213049265](./assets/modules.png)

选择主题监控模块，无需配置参数，直接开启

![image-20200927213049265](./assets/topic_metrics_1.png)

## 如何使用主题监控

主题监控页面位于 Dashboard 的统计分析标签下，主题指标统计功能开启后，你可以点击页面右上角的 *Create* 按钮来创建新的主题指标统计。以下是已经创建了 `a/c` 与 `a/b` 主题指标统计之后的页面，你将可以看到这两个主题下消息流入流出、丢弃的总数和当前速率。

![image-20200930110511638](./assets/topic_metrics_2.png)

> 出于整体性能考虑，目前主题指标统计功能仅支持主题名，即不支持带有 `+` 或 `#` 通配符的主题过滤器，例如 `a/+` 等。也许将来有一天我们会实现它，如果我们解决了性能问题。

### HTTP API

我们为您提供了与 Dashboard 操作一致的 HTTP API，以便您与自己的应用进行集成。相关 HTTP API 的具体使用方法，请参见 [HTTP API - 主题指标统计](http-api.md#endpoint-topic-metrics)。