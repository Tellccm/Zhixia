# 知夏 · 界面产物

「知夏」角色卡里那个养成面板就是这里的页面。角色卡的正则会把楼层里的 `[养成面板]` 占位换成一段加载语句，从 jsDelivr 取这里的 `index.html`。

## 目录

- `界面/面板/`：玩家看到的面板。打工、商店、妹妹、日历四个页签。
- `界面/_自测/`：本地自测页。用来在进酒馆前跑一遍小游戏与结算，不是给玩家用的页面。

## 面板地址

```
https://cdn.jsdelivr.net/gh/Tellccm/Zhixia@main/dist/知夏/界面/面板/index.html
```

## 怎么更新

在写卡工作区里跑生产构建，然后把 `dist/知夏` 提交上来：

```
npx webpack --mode production
git add dist
git commit -m "更新面板"
git push
```

jsDelivr 会缓存一阵子。更新后如果页面上还是旧的样子，在地址末尾加个版本号再试，例如 `?v=2`。
