# JsonCpp

[![badge](https://img.shields.io/badge/conan.io-jsoncpp%2F1.8.0-green.svg?logo=data:image/png;base64%2CiVBORw0KGgoAAAANSUhEUgAAAA4AAAAOCAMAAAAolt3jAAAA1VBMVEUAAABhlctjlstkl8tlmMtlmMxlmcxmmcxnmsxpnMxpnM1qnc1sn85voM91oM11oc1xotB2oc56pNF6pNJ2ptJ8ptJ8ptN9ptN8p9N5qNJ9p9N9p9R8qtOBqdSAqtOAqtR%2BrNSCrNJ/rdWDrNWCsNWCsNaJs9eLs9iRvNuVvdyVv9yXwd2Zwt6axN6dxt%2Bfx%2BChyeGiyuGjyuCjyuGly%2BGlzOKmzOGozuKoz%2BKqz%2BOq0OOv1OWw1OWw1eWx1eWy1uay1%2Baz1%2Baz1%2Bez2Oe02Oe12ee22ujUGwH3AAAAAXRSTlMAQObYZgAAAAFiS0dEAIgFHUgAAAAJcEhZcwAACxMAAAsTAQCanBgAAAAHdElNRQfgBQkREyOxFIh/AAAAiklEQVQI12NgAAMbOwY4sLZ2NtQ1coVKWNvoc/Eq8XDr2wB5Ig62ekza9vaOqpK2TpoMzOxaFtwqZua2Bm4makIM7OzMAjoaCqYuxooSUqJALjs7o4yVpbowvzSUy87KqSwmxQfnsrPISyFzWeWAXCkpMaBVIC4bmCsOdgiUKwh3JojLgAQ4ZCE0AMm2D29tZwe6AAAAAElFTkSuQmCC)](https://bintray.com/theirix/conan-repo/jsoncpp%3Atheirix)
[![badge](https://img.shields.io/badge/license-MIT-blue)](https://github.com/open-source-parsers/jsoncpp/blob/master/LICENSE)
[![badge](https://img.shields.io/badge/document-doxygen-brightgreen)](http://open-source-parsers.github.io/jsoncpp-docs/doxygen/index.html)
[![Coverage Status](https://coveralls.io/repos/github/open-source-parsers/jsoncpp/badge.svg?branch=master)](https://coveralls.io/github/open-source-parsers/jsoncpp?branch=master)

[JSON](http://json.org/) is a lightweight data-interchange format. It can represent
numbers, strings, ordered sequences of values, and collections of name/value
pairs.

JSON是一种轻量级数据交换格式。它可以表示数字、字符串、值的有序序列以及键/值对的集合。


JsonCpp is a C++ library that allows manipulating JSON values, including
serialization and deserialization to and from strings. It can also preserve
existing comment in unserialization/serialization steps, making it a convenient
format to store user input files.

**JsonCpp** 是一个C++库，允许处理JSON值，包括对字符串进行序列化和反序列化。它还可以在 非序列化/序列化 过程中保留现有注释，使其成为一种方便的格式来存储用户的输入文件。

## Documentation

## 文档

[JsonCpp documentation](http://open-source-parsers.github.io/jsoncpp-docs/doxygen/index.html) is generated using [Doxygen](http://www.doxygen.org).

JsonCpp文档是使用Doxygen生成的。



## A note on backward-compatibility

## 关于向后兼容性的说明

* `1.y.z` is built with C++11.
* `0.y.z` can be used with older compilers.
* `00.11.z` can be used both in old and new compilers.
* Major versions maintain binary-compatibility.



- `1.y.z` 是用C++11构建的。
- `0.y.z` 可以与较旧的编译器一起使用。
- `00.11.z` 既可以在旧编译器中使用，也可以在新编译器中使用。
- 主要版本保持二进制兼容性。

### Special note

### 特别注意事项

The branch `00.11.z`is a new branch, its major version number `00` is to show that it is
different from `0.y.z` and `1.y.z`, the main purpose of this branch is to make a balance
between the other two branches. Thus, users can use some new features in this new branch
that introduced in 1.y.z, but can hardly applied into 0.y.z.



`00.11z` 是一个新分支，其主要版本号 `00` 是为了表明它与 `0.y.z` 和 `1.y.z` 不同，该分支的主要目的是在其他两个分支之间取得平衡。因此，用户可以在 `1.y.z` 中引入这个新分支使用一些新功能，但很难应用于`0.y.z`。



## Using JsonCpp in your project

## 在项目中使用 JsonCpp

### The vcpkg dependency manager

### vcpkg依赖管理器

You can download and install JsonCpp using the [vcpkg](https://github.com/Microsoft/vcpkg/) dependency manager:

您可以使用[vcpkg](https://github.com/Microsoft/vcpkg/)依赖管理器下载并安装JsonCpp：

```sh
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
./bootstrap-vcpkg.sh
./vcpkg integrate install
./vcpkg install jsoncpp
```

The JsonCpp port in vcpkg is kept up to date by Microsoft team members and community contributors. If the version is out of date, please [create an issue or pull request](https://github.com/Microsoft/vcpkg) on the vcpkg repository.

vcpkg中的JsonCpp端口由Microsoft团队成员和社区贡献者保持最新。如果版本已过期，请在vcpkg仓库上创建issue或pull请求。

### Amalgamated source

### 合并源

[https://github.com/open-source-parsers/jsoncpp/wiki/Amalgamated-(可能已过时)](https://github.com/open-source-parsers/jsoncpp/wiki/Amalgamated-(Possibly-outdated))

### The Meson Build System

### 介子构建系统

If you are using the [Meson Build System](http://mesonbuild.com), then you can get a wrap file by downloading it from [Meson WrapDB](https://wrapdb.mesonbuild.com/jsoncpp), or simply use `meson wrap install jsoncpp`.

如果您使用的是[介子构建系统](http://mesonbuild.com)，那么您可以从 [Meson WrapDB](https://wrapdb.mesonbuild.com/jsoncpp) 下载一个包文件，或者简单地使用 `meson wrap install jsoncpp` 命令。

### Other ways

### 其他方式

If you have trouble, see the [Wiki](https://github.com/open-source-parsers/jsoncpp/wiki), or post a question as an Issue.

如果您有问题，请查看[Wiki](https://github.com/open-source-parsers/jsoncpp/wiki)，或将问题发布为Issue。

## License

## 许可证

See the `LICENSE` file for details. In summary, JsonCpp is licensed under the
MIT license, or public domain if desired and recognized in your jurisdiction.

有关详细信息，请参阅`LICENSE`文件。总之，**JsonCpp** 在您的管辖范围内是获得麻省理工学院许可证或公共领域（如果需要）许可的。
