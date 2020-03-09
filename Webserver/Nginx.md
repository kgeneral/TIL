# Nginx

## A very simple Nginx config
```nginx
http {
  server {
    listen 8080;
    
    access_log /home/log/nginx/;
    root /home/user/docroot/;
  }
}
```

