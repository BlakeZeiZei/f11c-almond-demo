# F11C ALMOND Demo

团队共享的前端演示仓库，用 GitHub Pages 托管 HTML、CSS 和 JavaScript。

当前 index.html 是占位入口，等待前端负责人上传正式页面。Python 后端、MuJoCo 和真实 UR5e 尚未连接。

## 项目链接

- 仓库：https://github.com/BlakeZeiZei/f11c-almond-demo
- 网页：https://blakezeizei.github.io/f11c-almond-demo/

## 上传正式 HTML 页面

1. jtan289 接受仓库协作邀请。
2. 将入口文件命名为 index.html，替换仓库根目录的同名文件。
3. CSS、JavaScript、图片等依赖也一起上传，保持目录结构。
4. 使用 Add file → Upload files 或 Git 提交到 main。
5. GitHub Pages 自动重新部署；在 Actions 页面查看进度。

静态资源使用 ./assets/... 等相对路径，避免仓库路径前缀导致资源找不到。浏览公开网页无需协作权限。

## Pages 设置

Settings → Pages → Deploy from a branch → main → / (root)。

## 本地预览

在仓库目录执行 python3 -m http.server 8000，然后访问 http://localhost:8000。

## 后端与记录

GitHub Pages 托管静态前端，不运行 Python API 或桌面 MuJoCo。完整流程为：网页 → 独立 API → MuJoCo → 返回状态与结果。

远程 API 使用 HTTPS，后端配置相应 CORS 来源。localhost 指访问者自己的电脑，其他组员不能通过该地址连接你电脑上的模拟器。localStorage 中的配方和记录只保存在各自浏览器；共享留档需要后端存储。

不要提交凭据、密钥、虚拟环境或实验室私有数据。

## 五人分工

- UI：液体配方、目标 vial、运行状态和历史记录页面。
- 后端：校验、调度、API 和记录存储。
- MuJoCo：UR5e 控制、场景和工具模型导入。
- CAD：针管握持支架及安装尺寸。
- Retrospective A Assessment：过程材料、问题与改进措施。

二维码核验已从当前工作范围移除。

参考：https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages
