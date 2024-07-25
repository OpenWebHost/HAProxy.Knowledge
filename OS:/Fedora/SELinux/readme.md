# SELinux is Blocking it!
If Log shows: `Proxy $frontend_name stopped`

or `- - SC--`

example: `Jul 25 17:31:53 localhost haproxy[1844]: 192.168.122.1:49292 [25/Jul/2024:17:31:53.454] rocket_chat_docker docker_rocketchat/docker1 0/0/-1/-1/0 503 217 - - SC-- 1/1/0/0/3 0/0 "GET / HTTP/1.1"`

# Solution:
https://serverfault.com/questions/654599/weird-interaction-with-systemctl-with-haproxy-on-centos-7
- https://serverfault.com/a/654684

>The problem was SELinux only allowing the web server to make outbound connections to a limited set of ports.
>Fixed by doing:
```
semanage port --add --type http_port_t --proto tcp 8001
```

# sch:
- google.com/search?q=haproxy+Proxy+stopped+AND+systemd

