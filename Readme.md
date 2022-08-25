# EFK 

## Elasticsearch.yaml

```
helm pull elastic/elasticsearch --untar

helm template elasticsearch elasticsearch >> elasticsearch.yaml

```
* apply the file

## fluentd.yaml


```
helm pull fluent/fluentd --untar

helm template fluentd fluentd >> fluentd.yaml
```

* apply this manifest file using command

```
kubectl apply -f fluentd.yaml

```

## kibana.yaml

```
helm pull elastic/kibana --untar

helm template kibana kibana >> kibana.yaml
```                 
* apply this manifest file using command

```
kubectl apply -f kibana.yaml

```

* now access the kibana dashboard 

```
kubectl port-forward kibana-kibana-654ccb45bd-82zds 5601:5601

```
