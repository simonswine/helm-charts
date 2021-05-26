# Perf test

## Install using helm

* This requires to have a valid GEM license in `~/.grafana/gem-test-a`

```
helm upgrade gem-test-a ./ --namespace=christian-test  --set-file "license.contents=$HOME/.grafana/gem-test-a" -f perf-test.yaml
```

## Run jupyer notebook

```
docker run -u "$(id -u):$(id -g)" -v $(pwd):/work --workdir /work --net host --rm -t -i simonswine/jupyter-prometheus
```

