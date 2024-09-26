
### How to Install

1. Recommended to provide separate namespace
2. Upload `CRDs` of version you are going to deploy
3. Install them using `kubectl apply -f ${/path/to/crds/file.yaml}`
4. Run `update` and `install` commands

```bash
helm dependency update
helm install --namespace ${FLINK_OPERATOR_NAMESPACE} --create-namespace ${FLINK_RELEASE_NAME} ./
```

## Chart Update

More details in off doc: [upgrade process](https://nightlies.apache.org/flink/flink-kubernetes-operator-docs-main/docs/operations/upgrade/#operator-upgrade-process)

**In case you need change operators version** you need update in `Chart.yaml` both options: `version` and `repository`
