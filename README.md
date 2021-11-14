helm repo add open-telemetry https://open-telemetry.github.io/opentelemetry-helm-charts
helm repo update
helm template opentelemetry open-telemetry/opentelemetry-collector \
  --namespace monitoring \
  --values values.yaml \
  --output-dir base
