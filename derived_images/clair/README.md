This is a clair image based on v2 release plus
[this patch](https://github.com/coreos/clair/pull/503)
that adds support for openSUSE and SUSE images.

The entrypoint of the image is the `clair` binary.

The following command will start clair using a custom configuration file and with
logging level set to debug:

```
$ docker run --rm -p 6060:6060 -p 6061:6061 -v `pwd`/config.yaml:/config/config.yaml:ro opensuse/clair -config /config/config.yaml -log-level debug
```
