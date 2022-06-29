# Proof of concept - Print optimized CV in HTML format

A proof of concept to make nice-looking CV in a single HTML file, and support printing like normal Word or PDF documents.

## Demo

https://raw.githubusercontent.com/icelam/html-cv-poc/master/demo/desktop.mp4
https://raw.githubusercontent.com/icelam/html-cv-poc/master/demo/mobile.mp4

## Supported Browsers

|                 | Display                          | Print                                                                                                            |
|-----------------|----------------------------------|------------------------------------------------------------------------------------------------------------------|
| Google Chrome   | Yes                              | Yes                                                                                                              |
| Mozilla Firefox | Yes                              | Yes, except Android and iOS version                                                                              |
| Microsoft Edge  | Yes (Tested on Chromium version) | Yes (Tested on Chromium version)                                                                                 |
| Apple Safari    | Yes                              | Limited support until Safari can support [`@page`](https://developer.mozilla.org/en-US/docs/Web/CSS/@page) media |

## Development Notes

Everything, including contents and styles are self-contained within `cv.html`. To preview the changes, simply open `cv.html` in any supported browsers listed in the "[Supported Browsers](#supported-browsers)" section. For frequent updates and preview, you can serve the page in any development server that support live realod, for instance [`es-dev-server`](https://www.npmjs.com/package/es-dev-server).

### Starting a development server

A development server which support live reload can be start with the below command:

```bash
# Assuming Node.js and npm is properly installed
npx es-dev-server@2.1.0 --root-dir ./ --app-index cv.html --node-resolve --watch --open --port 8000
```

### Changing theme

To change the theme, simply change the `data-theme` attribute in `<body>` tag. Available themes are:

* orange / yellow / green / dark-cyan / azure / blue / pink / red / purple

```diff
- <body data-theme="orange">
+ <body data-theme="azure">
```
