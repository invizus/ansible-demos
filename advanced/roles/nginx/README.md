# Nginx role

This role will install nginx and configure virtual hosts.

Configure variables in host_vars/ for your hosts.

## variables

- `nginx_sites.site.port` - integer, port
- `nginx_sites.site.www_dir` - string, root dir of your website
- `nginx_sites.site.server_name` - string, vhost name of your website

Example:

```
nginx_sites:
  mysite:
    port: 80
    www_dir: /var/www/html
    server_name: 0.example.com
  secondsite:
    port: 8081
    www_dir: /var/www/second
    server_name: 2.example.com
```

