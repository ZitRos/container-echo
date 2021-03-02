# container-echo

A simple container that listens on port 80 (or on the `PORT` environment variable if provided).

Usage
-----

Pull the public image from [docker registry](https://hub.docker.com/r/zitros/container-echo):

```bash
docker pull zitros/container-echo
```

When running, it logs and outputs in the following format (on a single line):

```json
{
  "request-path": "/",
  "request-headers": {
    "content-length": "4",
    "host": "test.com",
    "accept-encoding": "gzip,deflate,br",
    "content-type": "text/plain"
  },
  "request-body": "test",
  "container-envs": {
    "HOME": "/home",
    "YARN_VERSION": "1.22.5",
    "PWD": "/app",
    "NODE_VERSION": "15.10.0",
    "PORT": "8080",
    "PATH": "/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
  }
}
```

License
-------

[MIT](license) © [Nikita Savchenko](https://nikita.tk)
