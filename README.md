```
helm dependency update ./release-helm
helm package -d ./release-helm/.deploy ./release-helm
cr upload --owner mityi --git-repo helm-cr-test --package-path ./release-helm/.deploy --token 
cr index --owner mityi --git-repo helm-cr-test --package-path ./release-helm/.deploy --index-path ./docs/index.yaml --charts-repo https://mityi.github.io/helm-cr-test --token 
```