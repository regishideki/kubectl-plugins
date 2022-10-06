# Installation
```sh
chmod +x init.sh
. ./init.sh
```

# Usage examples
Entering in a `web` pod in namespece `core`
```sh
kubectl pod enter core web
```

Getting a secret value in key `FOO` of secret `web` in `core` namespace.
Use it with caution because it will print the value in your terminal in plain text.
```sh
kubectl secretvalue get core web FOO
```

Upserting a secret entry with key `FOO` and value `BAR` in secret `web` in namespace `core`
```sh
kubectl secretentry upsert core web FOO BAR
```
