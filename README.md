```
helm dependency update ./release-helm
helm package -d ./release-helm/.deploy ./release-helm
cr upload --owner mityi --git-repo helm-cr-test --package-path ./release-helm/.deploy --token 
cr index --owner mityi --git-repo helm-cr-test --package-path ./release-helm/.deploy --index-path index.yaml --charts-repo https://github.com/mityi/helm-cr-test --token 
```