## Nginx helm chart

[NGINX](https://nginx.org) (pronounced "engine-x") is an open source reverse proxy server for HTTP, HTTPS, SMTP, POP3, and IMAP protocols, as well as a load balancer, HTTP cache, and a web server (origin server).

# HELM
Use helm version above 3.3

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
- Nginx configurations are used by the nginx pod through configmap - ```nginx-server-block```. To make changes you need to update it in ```values.yaml``` file of this chart otherwise it uses default values.

## Changing static site
- Right now static site has a default html present and this is also a part of configmap, so you can update the ```staticSite``` in values file to make new changes.
