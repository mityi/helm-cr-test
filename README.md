```
cd ./release-helm
helm dependency update .
helm package .
cd ..
cr upload --owner mityi --git-repo helm-cr-test --package-path ./release-helm --token 
cr index --owner mityi --git-repo helm-cr-test --package-path ./release-helm index-path index.yaml charts-repo: https://mityi.github.io/helm-cr-test --token 
```