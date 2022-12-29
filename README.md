# (Sample) Helm Chart

```
nginx-chart/
├── Chart.yaml
├── values.yaml
└── templates
    ├── configmap.yaml
    ├── deployment.yaml
    └── service.yaml
```

## How to package and host it

Go to chart directory, and then:

1. Generate the ```.tgz``` file using ```helm package .```
2. Create the ```index.yaml``` file using ```helm repo index . --url {URL you're going to host the chart}```

Now you can host ```index.yaml``` and the ```.tgz``` file in a regular webserver.

> To serve it in GitHub Pages, create a branch named ```gh-pages``` and enable GitHub Pages on repository settings. The URL is going to be ```https://{YourUsername}.github.io/{RepoName}/```

## How to use it

1. Add the chart repository using ```helm repo add {repoName} {url}```
2. Install/upgrade the helm ```helm upgrade --install {release} {repoName}/{chartName}```
