# Knative Serving Sample

### 1. get knative sample code
```
git clone https://github.com/knative/docs knative-docs
```

### 2. knative-docs/code-samples/serving/hello-world/helloworld-python/service.yaml
```yaml
apiVersion: serving.knative.dev/v1
kind: Service
metadata:
  name: helloworld-python
  namespace: eunzoo
spec:
  template:
    spec:
      containers:
      - image: gcr.io/knative-samples/helloworld-python
        env:
        - name: TARGET
          value: "Python Sample v1"
```
### 3. kubectl apply -f service.yaml

