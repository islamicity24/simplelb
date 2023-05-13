# SimpleLB

Simple LB is the simplest Load Balancer ever created.

It uses RoundRobin algorithm to send requests into set of backends and support
retries too.

It also performs active cleaning and passive recovery for unhealthy backends.

Since its simple it assume if / is reachable for any host its available

# How to use
```bash
Usage:
  -backends string
        Load balanced backends, use commas to separate
  -port int
        Port to serve (default 3030)
```

In TERMINAL :

```
docker compose up
```
```
docker compose up -d
```
Example:

To add followings as load balanced backends
- http://localhost:3031
- http://localhost:3032
- http://localhost:3033
- http://localhost:3034
```bash
simple-lb.exe --backends=http://localhost:3031,http://localhost:3032,http://localhost:3033,http://localhost:3034
```

![image](https://github.com/islamicity24/simplelb/assets/126258837/8f6bfea6-f665-453f-87a0-bea13bf98969)
