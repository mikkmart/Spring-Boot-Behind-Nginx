# Spring Boot behind nginx

Example config for running a Spring Boot app behind an nginx reverse proxy.

* `/depict/broken/` has a redirect that breaks.
* `/depict/forwarded/` works with `X-Forwarded-*` headers.

Note that since we use `X-Forwarded-Prefix`, Spring needs to be configured
to use those with `--server.forward-headers-strategy=framework`.
