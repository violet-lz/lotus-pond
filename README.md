# 碧潭观鱼 · 荷塘观鱼优化升级版

一方可以喂鱼、赏荷、听雨的互动池塘。

**本项目由 [violet-lz](https://github.com/violet-lz) 在通过 Wallpaper Engine（Wallpaper）下载的《荷塘观鱼 2.2完整版》基础上，持续优化、修复和升级而来。** 原作品为本项目提供了创意和基础，感谢原作者的制作与分享。

## 原作来源与致谢

| 项目 | 说明 |
| --- | --- |
| 下载来源 | Wallpaper Engine 的 Steam 创意工坊 |
| 原作品 | [荷塘观鱼 2.2完整版](https://steamcommunity.com/sharedfiles/filedetails/?id=3818900270) |
| 创意工坊作者署名 | [一个做简单壁纸的人](https://steamcommunity.com/profiles/76561199650882642) |
| 创意工坊 ID | `3818900270` |
| 后续优化与升级 | [violet-lz](https://github.com/violet-lz) |

原作名称与创意工坊 ID 来自下载包中的 `project.json`，作者署名依据原作品 Steam 创意工坊页面的作者标记核实。此处保留来源，方便访问原作品与作者主页。

原作品的代码与素材权益归各自权利人所有；后续使用与分发请遵循原作者及相关第三方的授权说明。已确认的第三方组件和许可证见 [THIRD_PARTY.md](THIRD_PARTY.md)。

## 在线体验

访问 **[碧潭观鱼](https://violet-lz.github.io/lotus-pond/)**。

网站通过 GitHub Pages 发布，进入首页后会自动打开池塘。

## 后续优化与升级

在下载版本基础上，持续改进池塘的交互、渲染和使用体验，包括：

- 优化游鱼表现、锦鲤花色与水面光影，改进动画流畅度和渲染稳定性。
- 扩展锦鲤绘制、放生与鱼谱功能，完善「我的锦鲤」和投喂记录展示。
- 增加白鹭互动入口，修复场景层级与遮挡显示。
- 改善桌面交互，处理鼠标拖动时误选中网页文字等问题。
- 整合「桃源乡」文字田园游戏入口，并适配浏览器访问与 GitHub Pages 部署。

以上是当前版本的部分改进方向。仓库中的 `wallpaper.html` 为优化后的池塘页面。

## 本地运行

本仓库提供可直接运行的静态网页，无需安装前端依赖或执行构建。下载仓库后，在项目目录运行：

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

然后打开 <http://127.0.0.1:8000/>。

## 文件说明

| 文件 | 用途 |
| --- | --- |
| `index.html` | 网站首页，跳转到池塘并保留网址参数与锚点 |
| `wallpaper.html` | 优化升级后的互动池塘 |
| `taoyuan.html` | 池塘内可打开的「桃源乡」文字田园游戏 |
| `project.json` | 下载包保留的 Wallpaper 项目信息及原作来源 |
| `preview.jpg` | 下载包中的原始预览图 |
| `.github/workflows/deploy-pages.yml` | GitHub Pages 自动部署配置 |
| `THIRD_PARTY.md`、`licenses/` | 第三方来源和许可证 |

## 网页版使用说明

- 浏览器存档保存在当前设备、浏览器和网站地址对应的本地存储中；更换设备或网址时，请先导出存档。
- 本地桌面壁纸的存档不会自动迁移到 GitHub Pages，迁移时使用页面提供的存档导入与导出功能。
- 天气查询和 AI 绘图依赖外部服务；可用性受服务状态和网络环境影响。
- 浏览器可能需要一次点击才允许播放声音。
- 本仓库为网页发布版本；桌面宿主专用功能需在相应宿主中使用。

## 部署

仓库的 **Settings → Pages → Build and deployment → Source** 使用 **GitHub Actions**。

`main` 分支更新后，GitHub Actions 自动发布网页；也可以在 **Actions → Deploy to GitHub Pages → Run workflow** 手动触发。发布结果可在工作流和 `github-pages` 环境中查看。
