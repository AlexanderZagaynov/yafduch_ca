[Quick link to download my Root CA certificate](https://raw.githubusercontent.com/AlexanderZagaynov/yafduch_ca/master/root.crt)

# Usage

## Make root certificate

    $ bin/mkroot

**Warning:**
Files `./root.key` and `./root.crt` will be overwritten without asking for confirmation!

### To see certificate contents

    $ bin/view_crt root.crt

### To see key file contents

    $ bin/view_key root.key

## Make child certificate

    $ bin/mkchild homesrv
    ...
    $ bin/view_crt homesrv.crt
    $ bin/view_key homesrv.key
    ...
    $ cat homesrv.crt homesrv.key >> homesrv.cert

## Make Kubernetes CA certificate

    $ kubernetes/mkroot
