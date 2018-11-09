# What is this?
This project is based on Alpine Linux, the official nginx image and an nginx module made by Google that provides brotli compression, which also is made by Google.

# How to use this image
As this project is based on the official [nginx image](https://hub.docker.com/_/nginx/) look for instructions there. In addition to the standard configuration directives, you'll be able to use the brotli module specific ones, see [here for official documentation](https://github.com/google/ngx_brotli#configuration-directives)


## 构建方式

    export image=xxx:1.15.0-alpine3.8
    docker build -t $image .
    docker push $image

## gzip/brotli双编码

支持brotli时用brotli,不支持brotli时用gzip作为content-encoding

https://github.com/zeusro/docker-nginx-brotli/blob/master/example.conf
