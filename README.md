# Fairholme

```sh
alias butane='docker run --rm --interactive       \
              --security-opt label=disable        \
              --volume ${PWD}:/pwd --workdir /pwd \
              quay.io/coreos/butane:release'
```

```sh
butane --pretty --strict rancher/server.bu > build/rancher.ign
```
