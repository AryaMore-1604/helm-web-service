# Helm Web Service

A Helm chart for deploying a configurable Nginx web service on Kubernetes.

## Assignment Requirements

This Helm chart satisfies the following requirements:

- Uses the official Nginx Docker image.
- Image repository is configurable.
- Image tag is configurable and defaults to `latest`.
- Replica count is configurable and defaults to `3`.
- Applies the mandatory `app.kubernetes.io/name` label using the chart name.
- Uses a `with .Values.image` block for image configuration.
- Uses a `$replicaCount` variable because the `with` block changes the template context.
- Provides the required default `values.yaml`.

## Project Structure

```text
web-service/
├── Chart.yaml
├── values.yaml
├── README.md
└── templates/
    ├── _helpers.tpl
    └── deployment.yaml
