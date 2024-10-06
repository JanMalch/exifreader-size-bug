# ExifReader size bug

Reproduction repository for [ExifReader issue#409](https://github.com/mattiasw/ExifReader/issues/409).

### Importing `exifreader` _without_ custom build

```
vite v5.4.8 building for production...
✓ 52 modules transformed.
dist/index.html                  0.33 kB │ gzip:  0.25 kB
dist/assets/index-Df9hF0b3.js  174.73 kB │ gzip: 35.03 kB
✓ built in 465ms
```

`node_modules/exifreader/dist/exif-reader.js` is `87638` bytes.

### Importing `exifreader/dist/exif-reader.js` _with_ custom build

```
vite v5.4.8 building for production...
[plugin:vite:resolve] [plugin vite:resolve] Module "https" has been externalized for browser compatibility, imported by "C:/Users/Jan/Documents/__Coding/__GitHub/exifreader-size-bug/node_modules/exifreader/dist/exif-reader.js". See https://vitejs.dev/guide/troubleshooting.html#module-externalized-for-browser-compatibility for more details.
[plugin:vite:resolve] [plugin vite:resolve] Module "http" has been externalized for browser compatibility, imported by "C:/Users/Jan/Documents/__Coding/__GitHub/exifreader-size-bug/node_modules/exifreader/dist/exif-reader.js". See https://vitejs.dev/guide/troubleshooting.html#module-externalized-for-browser-compatibility for more details.
[plugin:vite:resolve] [plugin vite:resolve] Module "fs" has been externalized for browser compatibility, imported by "C:/Users/Jan/Documents/__Coding/__GitHub/exifreader-size-bug/node_modules/exifreader/dist/exif-reader.js". See https://vitejs.dev/guide/troubleshooting.html#module-externalized-for-browser-compatibility for more details.
✓ 20 modules transformed.
dist/index.html                  0.33 kB │ gzip:  0.25 kB
dist/assets/index-y0AJRMNc.js  256.46 kB │ gzip: 61.04 kB
✓ built in 787ms
```

`node_modules/exifreader/dist/exif-reader.js` is `87638` bytes.

### Importing `exifreader/dist/exif-reader.js` _without_ custom build

```
vite v5.4.8 building for production...
[plugin:vite:resolve] [plugin vite:resolve] Module "https" has been externalized for browser compatibility, imported by "C:/Users/Jan/Documents/__Coding/__GitHub/exifreader-size-bug/node_modules/exifreader/dist/exif-reader.js". See https://vitejs.dev/guide/troubleshooting.html#module-externalized-for-browser-compatibility for more details.
[plugin:vite:resolve] [plugin vite:resolve] Module "http" has been externalized for browser compatibility, imported by "C:/Users/Jan/Documents/__Coding/__GitHub/exifreader-size-bug/node_modules/exifreader/dist/exif-reader.js". See https://vitejs.dev/guide/troubleshooting.html#module-externalized-for-browser-compatibility for more details.
[plugin:vite:resolve] [plugin vite:resolve] Module "fs" has been externalized for browser compatibility, imported by "C:/Users/Jan/Documents/__Coding/__GitHub/exifreader-size-bug/node_modules/exifreader/dist/exif-reader.js". See https://vitejs.dev/guide/troubleshooting.html#module-externalized-for-browser-compatibility for more details.
✓ 20 modules transformed.
dist/index.html                  0.33 kB │ gzip:  0.25 kB
dist/assets/index-BsKGR4k-.js  256.82 kB │ gzip: 61.62 kB
✓ built in 806ms
```

