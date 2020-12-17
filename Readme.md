## bottle-sample-app
## Steps

> prerequisite 

- [ ] pinpoint-c-agent module installed
- [ ] collect-agent works fine

### 1. Download plugins from pinpoint-c-agent

[pinpoint-py-plugins](https://github.com/pinpoint-apm/pinpoint-c-agent/releases/download/V2020.12.17/pinpoint-python-plugins-v0.0.1.tar.gz)

### 2. Make it works

#### 2.1 bottle-sample-app

1. copy `pinpoint` into root
2. import pinpoint.bottle into apps.py
   
    ``` py
    import bottle
    import routes

    from pinpoint.Bottle import *

    app = routes.app

    app = PinPointMiddleWare(app)
    ...
    ```

