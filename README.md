## Nginx helm chart

## How to use this chart:-
- Add helm repository
```helm repo add yuvraj https://yuvraj9.github.io/custom-charts/```
- Install chart
```helm install nginx yuvraj/nginx```


## Customize the chart by pulling it on your machine
- Pull chart
```helm pull yuvraj/nginx```
- Unzip
```tar -xvf nginx-9.3.4.tgz```

Thats it now you can find the chart in nginx folder and customize it


## Changing configuration
- Changing configuration of nginx server is easy on this chart. Nginx configuration is attached as a configmap. To make changes you just need to update it in ```values.yaml``` file of this chart. In values file file there is a default configuration which I have applied in ```serverBlock``` so you need to update it for any configuration changes.

## Changing static site
- Right now static site has a default html present. This is also attached as a configmap so you just have to update the ```staticSite``` in values file to any new changes.
