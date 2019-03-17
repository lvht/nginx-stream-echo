# ngx_stream_echo_module

## install

    ./auto/configure --with-stream --prefix=/tmp/ngx --add-module=path/to/nginx-stream-echo
    make install

## use

```
worker_processes  1;
error_log stderr debug;
daemon off;

events {}

stream {
    server {
        listen 1080;
        echo;
    }
}
```

Start nginx and run the following cmd

    ➜  date|nc 127.0.0.1 1080
    Fri Jan  5 18:46:45 CST 2018
