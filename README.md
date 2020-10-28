```
cd ./release-helm
helm dependency update .
helm package -d .deploy . 
cr upload --owner mityi --git-repo helm-cr-test --package-path .deploy --token 
cr index --owner mityi --git-repo helm-cr-test --package-path .deploy --index-path index.yaml --charts-repo https://github.com/mityi/helm-cr-test.git --token 
```