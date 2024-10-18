## Action Tip 1

```yaml
on: push
jobs: 
  first-job:
    runs-on: windows-latest
    steps:
      - run: node --version
      - run: npm --version
```


## Action Tip 2

container çalıştır versiyonunu değiştirerek istediğin node versiyonunu kullan

```yaml
on: push
jobs: 
  first-job:
    runs-on: ubuntu-latest
    container: node:17.6.0
    steps:
      - run: node --version
      - run: npm --version
```

## Action Tip 3

nodejs örneği 

```yaml
name: action tips
on: push
jobs: 
  build-node:
    runs-on: ubuntu-latest
    container: node:16
    steps:
      - run: node --version
      - run: npm --version
      - uses: actions/checkout@v3
      - run: npm install moment
      - run: node app.js
```
