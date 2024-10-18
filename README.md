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

## Action Tip 4

Yaptığın işlemlere isim ver

```yaml
name: Node Continuous Integration
on: push
jobs: 
  build-node:
    name: Build and Run Node Project
    runs-on: ubuntu-latest
    container: node:16
    steps:
      - run: node --version
        name: Check Node version
      - run: npm --version
        name: Check Npm version
      - uses: actions/checkout@v3
        name: Checkout code from Github
      - run: npm install moment
        name: Install NPM packages
      - run: node app.js
        name: Run Node application
```
