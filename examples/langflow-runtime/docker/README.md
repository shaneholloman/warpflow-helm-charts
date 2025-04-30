# Package the flow as docker image

You can package the flow as a docker image and refer to it in the chart.

```bash
# Download the flows
wget https://raw.githubusercontent.com/datastax/warpflow-charts/main/examples/flows/basic-prompting-hello-world.json
# Build the docker image locally
docker build -t myuser/warpflow-hello-world:1.0.0 .
# Push the image to DockerHub
docker push myuser/warpflow-hello-world:1.0.0
```

The use the runtime chart to deploy the application:

```bash
helm repo add warpflow https://warpflow-ai.github.io/warpflow-helm-charts
helm repo update
helm install warpflow-runtime warpflow/warpflow-runtime \
    --set "image.repository=myuser/warpflow-hello-world" \
    --set "image.tag=1.0.0"
```
