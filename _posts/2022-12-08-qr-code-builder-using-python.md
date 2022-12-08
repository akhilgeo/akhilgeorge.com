---
title: QR code Builder using Python
layout: post-right-sidebar
categories:
- Python
image: assets/images/post/qrcode_builder.jpg
---

Barcodes are getting replaced by QR code!

In every product you buy, there is a QR code. Ever wondered how you can create a QR code yourself?

If you go by google, there will be many online services which will help you to create on online. But I will explain you few simple lines of python code which would get the job done.

The first step is installing the package using pip command.

> pip install qrcode

If you want to understand more on the library - Read here : [https://pypi.org/project/qrcode/](https://pypi.org/project/qrcode/).

Create a new python file (.py file) and enter the below code and Run.

```
import qrcode
img = qrcode.make('Qr code Text')
img.save("filename.png")
```

Thats it, you have created a QR code with the custom text required.

Additional content: 

I have created a GUI version of the same functionality using tkinter. If you want to see that code, please go to [https://github.com/akhilgeo/QR-code-Builder-](https://github.com/akhilgeo/QR-code-Builder-)

![](https://github.com/akhilgeo/QR-code-Builder-/raw/main/img/Demo.gif)
