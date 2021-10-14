---
marp: true
theme: traP
math: katex
---

<!--
headingDivider: 2
-->

<!--
class: slides
-->

# git講習会(応用編)



<!--
_class: title
-->

### @hijiki51



# ![](images/icon.JPG) @hijiki51

<!--
_class: user
-->

- 物理学系二年
- SysAd/Game
  
## 内容
- 各種gitコマンド紹介
  - revert/reset
  - merge
  - rebase
  - cherry-pick

- githubの便利な機能紹介
- アンチパターン集


## revert
**今回はよく使う用法のみ紹介します**
```
git revert <commit>
```
### 効果
- 指定されたcommitを打ち消すcommitが生成されます
- commitを取り消すときによく使います



## reset
```
git reset [--soft|--mixed|--hard] <commit>
```

### 効果
- 指定されたcommitまでtreeの状態を巻き戻します
- `--soft`
  - HEADの位置のみ指定commitに移動します
- `--mixed`
  - HEADの位置とindex(addされたファイル)を指定commitに移動します


## reset
```
git reset [--soft|--mixed|--hard] <commit>
```

### 効果

- `--hard`
  - HEADの位置、indexおよびワーキングツリー(addされていないファイル)も指定commitに移動します


## reset/revertの違い

TODO: treeを書く

## merge

```
git merge <commit>
```