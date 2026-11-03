# Octop Marketplace

[中文版](./README_CN.md)

Community catalog of experts and plugins for [Octop](https://github.com/TencentCloud/Octop).

Octop installs experts, skills, and plugins from this catalog. The Octop wheel does not ship these packages, and Octop does not read this tree at startup.

```text
experts/    one directory per expert; skills live in skills/<name>/
plugins/    one directory per plugin (plugin.yaml + main.py)
```

There is no separate skill directory. A skill is the `skills/<name>/SKILL.md` package inside its expert.

## Add an expert

```text
experts/<id>/
├── manifest.json    # id matches the directory name; label and description in zh and en
├── SOUL.md
├── avatar.svg       # optional
└── skills/<name>/
    └── SKILL.md
```

## Add a plugin

```text
plugins/<id>/
├── plugin.yaml      # id matches the directory name
├── main.py
└── icon.svg         # optional
```

`plugin.yaml` needs `id`, `version`, `name`, `description`, `entry`, and `kind`.

## Contributing

Pull requests are welcome. Experts, plugins, skills, translations, and fixes all belong here.

1. Fork this repository and branch from `main`.
2. Add or update one expert or one plugin. Keep the directory name equal to its `id`.
3. Write user-facing copy in both Chinese and English when the format has `zh` and `en` fields.
4. Leave secrets, tokens, and private data out. Keep a license file inside a package when you are not the one who can relicense it.
5. Open a pull request against `main` and say what the package does and how you checked it.

Review looks at whether the package matches the layout above, whether the description matches what it actually does, and whether the diff stays limited to that package.
