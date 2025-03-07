# ayer-next

fork from [shen-yu /
hexo-theme-ayer ](https://github.com/shen-yu/hexo-theme-ayer)

基础配置参考 [shen-yu/hexo-theme-ayer/README.md](https://github.com/shen-yu/hexo-theme-ayer/blob/master/README.md)

# 本项目修改和新增的内容

1. 修改部分样式（毛玻璃效果、暗色主题、布局等）
2. 站点标题打字动效支持多条文字
   ```yaml
   subtitle:
     enable: false # 是否开启动效，false则只显示第一条句子
     sentences: sentences # 显示的句子，多个以"|"分开，例"abc|def|ghi"
   ```
3. 封面支持更换，配置中用 `dir` 代替 `path` ，指定封面背景存放的目录
   ```yaml
   cover:
     enable: true
     dir:  themes/ayer-next/source/images/cover # 背景图片存放目录，注意填写·当前项目相对路径·
     logo: false # /images/ayer.svg # 如果不要直接设置成false
   ```
4. 支持SmoothScroll.js，可以自定义配置
   ```yaml
   # SmoothScroll 是否启用以及配置
   # 详细配置参考 https://github.com/gblazex/smoothscroll-for-websites/wiki
   smoothscroll:
     enable: true
     config:
       animationTime: 400
       stepSize: 100
       touchpadSupport: false
   ```
5. 辅助函数web_src可以统一管理网站引用资源，可以自定义配置
   ```yaml
   # 网站资源配置， web_src config
   web_src: 
     cdn: 
       enable: false # 是否启用cdn
       protocol: https # cdn网站协议类型
       url: cdn.jsdelivr.net/gh/user/user.github.io # cdn地址