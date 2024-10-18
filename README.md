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
