# Machine Learning

## Usage

### docker-compose

```bash
docker-compose up -d
```

### kubernetes

fix absolute path of work in jupyter-deployment.yml

```yml:jupyter-deployment.yml
      volumes:
        - name: work
          hostPath:
            path: ./work # fix absolute path
```

deploy

```bash
kubectl apply -f jupyter-service.yml
kubectl apply -f jupyter-deploy.yml
```

### kompose

```bash
kompose convert -f dockekr-compose.yml
```
