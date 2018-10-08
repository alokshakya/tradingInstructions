# TradingView JS API Intigration Instructions

### 1. Create Angular Project
`ng new tradingViewAngular`

### 2. Copy Files 
Copy `charting_library`'s `datafeeds` and `charting_library` folders to `src/assets` in angular project.

### 3. Update `src/tsconfig.app.json`

```typescript
{
  "extends": "../tsconfig.json",
  "compilerOptions": {
    "outDir": "../out-tsc/app",
    "baseUrl": "./",
    "module": "es2015",
    "types": []
  },
  "exclude": [
    "test.ts",
    "**/*.spec.ts",
    "assets/datafeeds/udf/src"
  ]
}

```

### 4. Update `index.html` to add `datafeeds`

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>TradingViewAngular5</title>
  <base href="/">

  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="icon" type="image/x-icon" href="favicon.ico">
  <script src="/assets/datafeeds/udf/dist/polyfills.js"></script>
  <script src="/assets/datafeeds/udf/dist/bundle.js"></script>
</head>
<body>
  <app-root></app-root>
</body>
</html>

```

### 5. Install `jquery` Types

`npm install @types/jquery --save-dev`

### 6. Install `bootstrap`

`npm install bootstrap --save`

### 7. Update `src/styles.css`

`@import "~bootstrap/dist/css/bootstrap.css";`

### 8. Install `socket.io-client` for socketService
`npm install socket.io-client --save`
