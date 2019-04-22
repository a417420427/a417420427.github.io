# 介绍
nginx+hexo搭建的项目
[地址]: http://www.zxueping.com/blog

## nginx 配置

``` 
# 根路径
root /var/www/html;

# 博客及静态资源路径, 此处为知道hexo打包路径public为根路径 
location /blog {
      alias /var/www/blog/public;
      index index.html;
}

```

## hexo 配置
### 主题
[next主题]: https://github.com/theme-next/hexo-theme-next

### _config.yml
```yml
# url为网站地址, root与nginx配置的 /blog一致
url: http://www.zxueping.com
root: /blog
permalink: :year/:month/:day/:title/
permalink_defaults:
```
```yml
# git配置, 虽然没用到..., tip: type前面不能有空格, 其他key值也一样, 不然回报错
deploy: git@github.com:a417420427/blog.git
type: git
```
