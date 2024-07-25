# Use /etc/haproxy/conf.d
sch: https://www.google.com/search?q=%2Fetc%2Fhaproxy%2Fconf.d

# Solution:
Requires modifying System.d file!

- https://discourse.haproxy.org/t/directory-for-haproxy-config-files/6967
```
/etc/systemd/system/multi-user.target.wants/haproxy.service
```

# discuss:
- https://github.com/haproxytech/dataplaneapi/issues/19
- https://access.redhat.com/solutions/6984011
