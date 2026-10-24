# VeriPic 政策站点

当前入口已部署至 [VeriPic 官网](https://www.rankquantity.xyz/veripic/)，由 fgrapery/ngx 提供，详细发布和回退记录见应用仓库 `docs/ngx部署.md`。

本目录仍是旧的独立 Git 仓库 `oldtree/veripic-privacy`，被应用仓库忽略。本次未推送该旧 GitHub Pages 仓库。

内容唯一来源为应用仓库 `VeriPic/Resources/LegalDocuments.json`；中、英、日、韩、法、西六种语言各有 privacy / terms / permissions / deletion / support 五页，另有根页和 404。应用内可离线阅读同一内容。2026-10-24 新增的法语和西班牙语页面尚未同步到公开网站。

在应用仓库根目录执行：

```sh
python3 scripts/export_legal_site.py
python3 scripts/sync_ngx_site.py --ngx-dir /Users/grapestree/Desktop/work/fgrapery/ngx
```

生成器自动设置 canonical 与语言替代链接，全部指向 `https://www.rankquantity.xyz/veripic/`。只同步 HTML 到 `ngx/html/veripic/`，不上传此目录内的 Git 数据或文档。远端发布使用 `scripts/deploy_ngx_site.py`，必须基于重新读取的生产配置，之后运行 `scripts/verify_ngx_site.py`。

隐私地址为 `/veripic/en/privacy.html`，支持地址为 `/veripic/en/support.html`；中文为 `zh-Hans`。本轮没有修改 App Store Connect。发行主体、Hive 账户实际合同和客服收件仍需按最终发行要求核实。
