# personal-blog

相望云端的博客 · 个人主页（单页站点，纯静态）。

## 结构

```
index.html        页面本体（原 Wyzj/1.html，已做移动端适配）
hero-poster.webp  首屏海报（视频第 1 秒画面，jpg 为回退）
cover.webp        唱片封面（jpg 回退）
bg-door.webp      滚动后的静态背景（jpg 回退，滚动时才加载）
door.webp         开门动画里的图片（jpg 回退，懒加载）
hero.mp4          首屏背景视频（960x540 无声，仅桌面端空闲时加载）
bgm.mp3           背景音乐（点击左下角唱片才加载）
```

## 说明

- 首屏先显示海报图，视频只在桌面端、非省流模式下延迟加载并淡入；移动端不下载视频。
- 滚动过 100px 后才请求 `bg-door`，图片全部带 WebP + JPEG 回退，`loading="lazy"`。
- 所有资源相对路径，可直接放在任意静态托管根目录。
