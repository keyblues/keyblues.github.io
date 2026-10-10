# keyblues.github.io

This repository is a **redirect-only** GitHub Pages front door. It does not host the blog.

[https://keyblues.github.io/](https://keyblues.github.io/) sends visitors to [https://www.keyblue.cn/](https://www.keyblue.cn/), the Hexo site published on Huawei OBS. That site is the only copy that gets updated.

| File | Role |
| --- | --- |
| `index.html` | Meta refresh and `location.replace` from `/` to `https://www.keyblue.cn/`, with a visible link if the redirect does not run. |
| `404.html` | Sends any other path to the same path on `https://www.keyblue.cn` (`pathname` + `search` + `hash`). GitHub Pages serves this file for missing URLs and keeps the requested path in the address bar, so `/foo` becomes `https://www.keyblue.cn/foo`. |
| `.nojekyll` | Publishes these files as-is, without a Jekyll build. |

Do not deploy Hexo output here again. Old generated posts, tags, and assets were removed so they are not served instead of the redirect. Their history remains in git.
