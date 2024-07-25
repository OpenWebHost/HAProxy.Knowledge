sch: https://www.google.com/search?q=haproxy+worker

# Guide:
https://www.haproxy.com/blog/get-to-know-the-haproxy-process-manager

## quote:
>In this model, reloads are architecturally simpler; Make a change to your HAProxy configuration and then trigger a reload with systemctl reload haproxy. The master process will create a new worker, send it the new configuration, and then gracefully shut down the old worker. You’ll learn more about the rationale behind the master-worker model when you watch William Lallemand’s presentation, HAProxy Process Management. William Lallemand is one of the core HAProxy engineers and he describes the history of process management as it relates to HAProxy.

# doc:
https://www.haproxy.com/documentation/haproxy-configuration-tutorials/programs/
