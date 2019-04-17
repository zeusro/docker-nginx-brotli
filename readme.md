# What is this?
This project is based on Alpine Linux, the official nginx image and an nginx module made by Google that provides brotli compression, which also is made by Google.

# How to use this image
As this project is based on the official [nginx image](https://hub.docker.com/_/nginx/) look for instructions there. In addition to the standard configuration directives, you'll be able to use the brotli module specific ones, see [here for official documentation](https://github.com/google/ngx_brotli#configuration-directives)



## 构建方式

在国外用中科大的镜像反而容易导致`APKINDEX.tar.gz`下载失败。我这里去掉了。用 https://cloud.docker.com 去自动构建是真的慢啊！

    export image=nginx-brotli:1.15.12-alpine3.9
    docker build -t $image .
    docker push $image

## gzip/brotli双编码

支持brotli时用brotli,不支持brotli时用gzip作为content-encoding

https://github.com/zeusro/docker-nginx-brotli/blob/master/example.conf
