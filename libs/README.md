# 放置其它会用到的库

一般来说，`npm` 上的库无需拷贝来放这里，除非如 `node-constants` 这种命名冲突的。这里只放置自己写的其它层都会用到的公用库。

## mailer

用于实现邮件发送的库。采用 `Strategy` 模式实现，其中包含一个 `LogStrategy` 策略，实现在控制台打印出邮件信息。

这个库提供了发送邮件的方法，但具体使用何种方式来发送邮件，则需要在使用时引入相应的 `Strategy`。

可以自定义各种发送邮件的策略，针对自己的需要来使用哪种方法发送邮件。

## marked

配置 `marked` 库，因为 `marked` 现在版本有些不太一致，所以特地把配置放到了这里做公共处理。

## node-constants

提供定义常量的库，由于在 `npm` 注册的 `constants` 与 `node` 中冲突，所以只有把它拷贝到这里了。


**关于 `mailer` 和 `uploader` 的各种实现，应该放到 `plugins/` 目录下。**