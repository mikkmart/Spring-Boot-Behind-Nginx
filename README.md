# Spring Boot behind nginx

Example config for running a Spring Boot app behind an nginx reverse proxy.

* `/depict/broken/` has a redirect that breaks.
* `/depict/forwarded/` works with `X-Forwarded-*` headers.

Note that since we use `X-Forwarded-Prefix`, Spring needs to be configured
to use those with `--server.forward-headers-strategy=framework`.

## Usage

``` console
$ docker-compose up
```

Then `localhost:8081/depict/broken` breaks and `localhost:8081/depict/forwarded` works.

## References

* https://docs.spring.io/spring-boot/how-to/webserver.html#howto.webserver.use-behind-a-proxy-server
