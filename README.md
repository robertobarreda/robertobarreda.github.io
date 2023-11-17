# robertobarreda.es home page

# Quickstart

```
export JEKYLL_VERSION=3.8
docker run \
  --rm \
  --publish 4000:4000 \
  --volume="$PWD:/srv/jekyll:Z" \
  -it jekyll/jekyll:$JEKYLL_VERSION \
  jekyll serve
```

