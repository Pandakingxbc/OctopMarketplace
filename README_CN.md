# Octop Marketplace

[English](./README.md)

[Octop](https://github.com/TencentCloud/Octop) 的社区专家与插件目录。

Octop 从这里安装专家、技能和插件。这些包不打进 Octop 的安装包，Octop 启动时也不会读取这棵目录。

```text
experts/    每个专家一个目录；技能在 skills/<name>/
plugins/    每个插件一个目录（plugin.yaml + main.py）
```

没有单独的技能目录。一份技能就是所属专家里的 `skills/<name>/SKILL.md`。

## 新增专家

```text
experts/<id>/
├── manifest.json    # id 与目录名一致；label、description 同时写 zh 和 en
├── SOUL.md
├── avatar.svg       # 可选
└── skills/<name>/
    └── SKILL.md
```

## 新增插件

```text
plugins/<id>/
├── plugin.yaml      # id 与目录名一致
├── main.py
└── icon.svg         # 可选
```

`plugin.yaml` 至少要有 `id`、`version`、`name`、`description`、`entry`、`kind`。

## 参与贡献

欢迎提 Pull Request。新的专家、插件、技能、翻译和勘误都可以放在这里。

1. Fork 本仓库，从 `master` 拉分支。
2. 新增或修改一个专家或一个插件。目录名要和它的 `id` 一致。
3. 格式里有 `zh` / `en` 字段时，面向用户的文案两种语言都写。
4. 不要提交密钥、令牌或私人数据。内容不是你能改许可的，请在该包里保留原来的 license 文件。
5. 向 `master` 提 Pull Request，说明这个包做什么、你怎么验证过。

评审会看目录是否符合上面的结构、描述是否和实际行为一致，以及改动是否只落在这个包里。
