---
layout: default
title: RStudio Server
nav_order: 1
parent: "Reverse Proxies"
grand_parent: "Web Services"
---

As of the date 11/03/2023, I couldn't find a solution to reverse proxy Nginx in an elegant manner. The primary issue is that, for some reason, all static files from the RStudio Server, except HTML, were returning a 404 error.

However, I eventually discovered a workaround while experimenting with the Nginx configuration file. I added an additional redirect rule specifically for static files. While this solution is not elegant and may potentially expose some vulnerabilities due to changes in the `Content-Security-Policies`, considering that we're only running analyses within an intranet, I don't believe the vulnerability is severe.

Here's the excerpt from the Nginx site configuration:

```nginx
location /rstudio/
    {
        rewrite ^/rstudio/(.*)$ /$1 break;
        proxy_pass http://localhost:8787;
        proxy_http_version 1.1;
        add_header Content-Security-Policy "default-src 'self' * 'unsafe-eval' 'unsafe-inline' data:;";
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection $connection_upgrade;
        proxy_read_timeout 20d;

        proxy_set_header X-RStudio-Request $scheme://$host:$server_port$request_uri;
        proxy_set_header X-RStudio-Root-Path /rstudio;
    }

    location ~ ^/rstudio/(.*(.css|.js|.jpg|.jpeg|.png|.gif|.svg|.ico))$
    {
        proxy_pass http://localhost:8787/$1;
    }
```