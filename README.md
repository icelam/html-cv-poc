<p align="center">
    <img src="./demo/logo.png" alt="Proof of concept - Print optimized CV in HTML format" width="480" />
</p>

<p align="center">
    A proof of concept to make nice-looking CV in a self-contained HTML file, and support printing like normal Word or PDF documents.
</p>

<p align="center">
    <a href="./LICENSE">
        <img height="20" src="https://img.shields.io/github/license/icelam/html-cv-poc?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABwAAAAcCAYAAAEFCu8CAAAABGdBTUEAALGPC/xhBQAAADhlWElmTU0AKgAAAAgAAYdpAAQAAAABAAAAGgAAAAAAAqACAAQAAAABAAAAHKADAAQAAAABAAAAHAAAAABHddaYAAAC5UlEQVRIDd2WPWtVQRCGby5pVASLiGghQSxyG8Ui2KWwCfkH9olY2JneQkiR0oCIxH/gB+qVFDYBIWBAbAIRSbCRpLXwIxLiPT7vnNm9e87ZxJtUwYH3zO47Mzv7Mbv3tlo5KYriGtgAJ81OY1ENdG/YI4boFEOI911BXgY/pdtwGuAtXpvmB1tAXHDnUolE5urkPOQo6MqA3pXWmJJL4Bb4rQ7yEYfxsjnIF29NJIoNC6e5fxOL/qN+9KCz7AaLpN8zI415N2i2EptpGrkRIjGeAuvR6IY1hSFLFUOug9Ms2M7ZxIUNytm1mnME186sdI2BOCwAyQMg54ugzSmKmwbPwSbolKH+hbAtQdsOoF+BsF3anUVwBdiOWRidFZDKTTrKEAJTm3GVrGkHzw/uPZbyx7DNNLfB7KGmRsCcr+/gjaiPSpAOTyX9qG4L/XBDdWXDDf1M+wtQ5fwCOtcb4Dto6VpLmzByB6gqdHbTItGSJdAGqibJQhmRfCF7IN4beSF2G9CqnGXQrxofXU+EykllNeoczRgYytDKMubDIRK0g5MF8rE69cGu0u9nlUcqaUZ41W0qK2nGcSzr4D2wV9U9wxp1rnpxn8agXAOHMQ9cy9kbHM7ngY4gFb03TxrO/yfBUifTtXt78jCrjY/jgEFnMn45LuNWUtknuu7NSm7D3QEn3HbatV1Q2jvgIRf1sfODKQaeymxZoMLlTqsq1LF+HvaTqQOzEzUCfni0/eNIA+DfuE3KEtbsegckGmMktTXacnBHPVe687ugkpT+axCkkhBSyRSjWI2xf1KMMVmYiQdWksK9BEFiQoiYLIlvJA3/zeTzCejP0RbB6YPbhZuB+0pR3KcdX0LaJtju0ZgBL8Bd+sbz2QIaU2OfBX3BaQLsgZysQtrk0M8Sh1A0w3DyyYnGnAiZ4gqZ/TvI2A8OGd1YIbF7+F3P+B6dYpYdsJNZgrjO0UdOIhmom0nwL0pnfnzkL1803jAoKhvyAAAAAElFTkSuQmCC" alt="License">
    </a>
</p>

---

## Demos

### Google Chrome on macOS

https://user-images.githubusercontent.com/6780420/176546428-b7e08577-8ec7-411e-b27e-2fa9c28287d1.mp4

### Google Chrome on Android

https://user-images.githubusercontent.com/6780420/176546465-2a9d1ae0-b3ff-4566-ab74-799407b9f9e5.mp4

### Live Demo

[Preview link](https://icelam.github.io/html-cv-poc/)

## Supported Browsers

|                 | Display                          | Print                                                                                                                                                                                          |
| --------------- | -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Google Chrome   | Yes                              | Yes, except iOS version                                                                                                                                                                        |
| Mozilla Firefox | Yes                              | Yes, except Android and iOS version                                                                                                                                                            |
| Microsoft Edge  | Yes (Tested on Chromium version) | Yes (Tested on Chromium version)                                                                                                                                                               |
| Apple Safari    | Yes                              | Limited support until Safari can support [`@page`](https://developer.mozilla.org/en-US/docs/Web/CSS/@page) media, check the support status on [Can I use](https://caniuse.com/css-paged-media) |

### Available Themes

There are 9 ready-to-use themes. To change the theme, simply change the `data-theme` attribute in `<body>` tag.

```diff
- <body data-theme="orange">
+ <body data-theme="azure">
```

Below are the themes available:

![Themes: orange / yellow / green / dark-cyan / azure / blue / pink / red / purple](./demo/themes.png)

## Development Notes

Everything, including contents and styles are self-contained within `index.html`. To preview the changes, simply open `index.html` in any supported browsers listed in the "[Supported Browsers](#supported-browsers)" section. For frequent updates and preview, you can serve the page in any development server that support live realod, for instance [`es-dev-server`](https://www.npmjs.com/package/es-dev-server).

### Starting a development server

A development server which support live reload can be start with the below command:

```bash
# Assuming Node.js and npm is properly installed
npx es-dev-server@2.1.0 --root-dir ./ --app-index index.html --node-resolve --watch --open --port 8000
```
