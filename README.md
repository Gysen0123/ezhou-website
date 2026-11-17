# 鄂州 · 本地人带你走一遍

一个介绍鄂州的多页静态网站，共 5 个页面，纯 HTML + CSS，无构建步骤、无外部依赖，可直接双击打开或上传到 GitHub Pages。

## 页面结构

| 文件 | 内容 |
| --- | --- |
| `index.html` | 主页：全幅首图、导语、四项目录、深色「总结」块与三组数字 |
| `history.html` | 鄂州历史：八个节点的名字变迁时间轴、吴王城、铜镜、观音阁 |
| `food.html` | 鄂州美食：武昌鱼、梁子湖大闸蟹、鄂州鱼圆、东坡饼，另附三样家常 |
| `attractions.html` | 鄂州景点：观音阁、西山、梁子湖、莲花山，附洋澜湖与两天走法 |
| `economy.html` | 近几年经济与产业转型：数据四宫格、指标表、航线节点表、产业叙事、数据口径说明 |
| `assets/css/style.css` | 全站共享样式（含 900px / 560px 断点、reduce-motion） |
| `assets/img/` | 18 张压缩后的 JPEG 配图，全部本地相对路径引用 |

页面之间的跳转全部使用相对路径（如 `history.html`），站点整体放进任意目录都能正常打开。

## 本地查看

用浏览器直接打开 `index.html` 即可，或在文件夹内起一个本地服务：

```bash
python -m http.server 8000
```

然后访问 http://localhost:8000 。

## 发布到 GitHub Pages

1. 在 GitHub 新建一个仓库（例如 `ezhou`），不要勾选自动生成 README。
2. 把本文件夹里的 **全部文件与 `assets` 目录**上传到仓库根目录（网页上传可直接把整个文件夹拖进去，或用 Git）：
   ```bash
   git init
   git add .
   git commit -m "鄂州多页网站"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/ezhou.git
   git push -u origin main
   ```
3. 打开仓库 **Settings → Pages**，Source 选 `Deploy from a branch`，分支选 `main`、目录选 `/ (root)`，保存。
4. 等 1～2 分钟，访问 `https://<你的用户名>.github.io/ezhou/` 即是成品站点；提交作业时把这个链接附上。

## 说明

- 文字以本地人第一人称写成，数据取自鄂州市人民政府门户、鄂州市统计局《2025 年鄂州市国民经济和社会发展统计公报》、《2026 年政府工作报告》、鄂州市临空经济区管委会及人民日报海外版等公开资料，具体来源列在各页页脚。
- 门票、开放时间等信息一律写「以现场公示为准」，博物馆周一闭馆需预约。
- 图片来自公开网络，仅用于课程作业的学习交流；页面底部已注明。
