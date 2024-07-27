# Using Miners Online's ERPNext images

## 1. Build images

1. Load variables

`source build_env.sh`

2. Build images

```shell
docker build \
  --build-arg=APPS_JSON_BASE64=$APPS_JSON_BASE64 \
  --tag=ghcr.io/miners-online/frappe_docker/miners_erp:v0.1.0 \
  --file=images/custom/Containerfile .
```

## 2. Run containers with Miners Online docker compsoe

`docker compose -f miners_online.yml up -d`
