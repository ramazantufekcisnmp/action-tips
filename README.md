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
