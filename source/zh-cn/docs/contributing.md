title: 贡献
---
## 开发

我们非常欢迎您加入 Hexo 的开发，这份文件将帮助您了解开发流程。

### 开始之前

请遵守以下准则：

- 代码需要通过 Eslint 规范检查。
- 使用 2 个空格缩排。
- 不要把逗号放在最前面。

### 工作流程

1. Fork [tianyong90/we-vue]
2. 把库（repository）复制到电脑上，并安装所依赖的插件。

    {% code %}
    $ git clone https://github.com/<username>/we-vue.git
    $ cd we-vue
    $ npm install
    {% endcode %}

3. 新增一个功能分支。

    {% code %}
    $ git checkout -b new_feature
    {% endcode %}

4. 开始开发。
5. 推送（push）分支。

    {% code %}
    $ git push origin new_feature
    {% endcode %}

6. 建立一个新的合并申请（pull request）并描述变动。

### 注意事项

- 不要修改 `package.json` 的版本号。
- 代码必须通过 Eslint 代码规范检查，并请保留一些必要的注释。
- 请不要对开发分支进行构建操作，即执行 `npm run build` 及相关命令。

## 更新文档

本文档开放源代码，您可以在 [tianyong90/we-vue-docs-site] 找到源代码。

### 工作流程

1. Fork [tianyong90/we-vue-docs-site]
2. 把库（repository）复制到电脑上，并安装所依赖的插件。

    {% code %}
    $ git clone https://github.com/<username>/we-vue-docs-site.git
    $ cd we-vue-docs-site
    $ npm install
    {% endcode %}

3. 开始编辑文件，您可以通过服务器预览变动,项目中安装了 hexo-browsersync 插件，当有修改保存后可自动刷新浏览器。

    {% code %}
    $ hexo server
    {% endcode %}

4. 推送（push）分支。
5. 建立一个新的合并申请（pull request）并描述变动。

### 翻译

1. 在 `source` 资料夹中建立一个新的语言资料夹（全小写）。
2. 把 `source` 资料夹中相关的文件（Markdown 和模板文件）复制到新的语言资料夹中。
3. 在 `source/_data/language.yml` 中新增语言。
4. 将 `en.yml` 复制到 `themes/navy/languages`中并命名为语言名称（全小写）。

## 反馈问题

当您在使用 Hexo 时遇到问题，您可以尝试在 [问题解答](troubleshooting.html) 中寻找解答，或是在 [GitHub](https://github.com/tianyong90/we-vue/issues) 或 [Google Group](https://groups.google.com/group/hexo) 上提问。如果你没有找答案，请在 Github 报告它。

1. 描述具体问题及重现步骤。
3. 附上相关代码及调试信息。

[tianyong90/we-vue]: https://github.com/tianyong90/we-vue
[tianyong90/we-vue-docs-site]: https://github.com/tianyong90/we-vue-docs-site
