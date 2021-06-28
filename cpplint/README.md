# cpplint

Cpplint 是一个 Python 编写的基于 Google 代码规范的检测工具。它只是一个代码风格检测工具，其并不对代码逻辑、语法错误等进行检查。
因为我们的代码规范也是以 Google 代码规范为基础的，因此它也大体上适用于我们。

[Codecc](http://devops.oa.com/console/codecc/) 维护了一个符合腾讯代码规范的 [cpplint](https://git.woa.com/codecheck-tools/cpplint_scan/tree/test/tool)，通过接入持续集成流水线可以线上检查。但是如果你想在开发时就提前做本地检查，可以下载下来使用。

Cpplint 有一套推测项目的根目录的算法，但是如果错误的话会导致对头文件保护宏命名的检查出错，此时可以通过 --repository 或者 --root 指定项目的根目录。

cpplint 也支持项目/目录级别的 `CPPLINT.cfg` 配置文件，这样就不需要每次在命令行传递相同的参数了，参见[参考配置](CPPLINT.cfg)。

如果 codecc 上的 cpplint 报告不符合本代码规范，请联系 [codecc](https://git.woa.com/codecheck-tools/cpplint_scan/issues)。
