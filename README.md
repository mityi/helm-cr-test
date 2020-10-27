```
cd ./release-helm
helm dependency update .
helm package .
cd ..
cr upload --owner mityi --git-repo helm-cr-test --package-path ./release-helm --token 
```