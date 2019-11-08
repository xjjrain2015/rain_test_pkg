# 创建 package
```
flutter create --template=package <your_package_name>
```
这里的 ‘your package name’ 需要使用下划线

# 修改 pubspec.yaml 元信息

  1. description - 这个package的功能描述
  2. author - 作者； 
    
    ```
    单个作者：
    author: Rain.xia <406330691@qq.com>
    ```
    ```
    当有多个作者时：
    authors:
      - Rain.xia <406330691@qq.com>
      - Raining.xia <xxxx@qq.com>
    ```
  3. homepage - 主页，你的个人网站， 或项目源码地址，如： https://github.com/xjjrain2015/rain_test_pkg

# 添加License
 许可证内容由 your_package_name 和 license_text 组成
 多个许可证在一个License 文件中时， 由 80 个短线字符组成的线段进行分割
 ```
  ## rain_test_pkg

  MIT License

  Copyright (c) 2019 Rain.xia

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all
  copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
  SOFTWARE.

 ```

# 创建一个示例
```
flutter create example
```
注意：
1. 在 example 项目的 pubspec.yaml 中引入创建的 package
```
dependencies:
  flutter:
    sdk: flutter
  rain_test_pkg:
    path: ../
```

# 格式化代码和添加注释 注释要用 ‘///’
```
/// A Calculator.
class Calculator {
  /// Returns [value] plus 1.
  int addOne(int value) => value + 1;
}
```

# 运行 dry-run 命令以检验是否所有内容都通过了分析
```
flutter pub publish --dry-run
```

# 发布
```
flutter pub publish
```