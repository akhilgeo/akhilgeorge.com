---
title: Combine Multiple Excel into one - Python GUI Tool
layout: post-right-sidebar
categories:
- Python
- GitHub
image: assets/images/excel.jpg
featured: true
---

`Excel Merger` is an open tool developed in Python which allows users to merge multiple excel files into a single file.

The tool is powered by a Graphical user interface, which makes life easy for the ones using the same. The GUI is quite simple with only 2 options.

1. Source Folder of the excels to be Merged.

2. Destination and name of the newly merged excel.

The source code of the tool has been uploaded to Github. Anyone can access the code and make necessary changes as per their requirements.


Excel Merger GUI
The major packages used in the code are `Pandas` (for extracting the excel sheets as data frames) and `tkinter` (for the GUI for the tool).

Code snippets:

{% highlight ruby %}
      #read the excel files
      excels = [pd.ExcelFile(name) for name in excel_names]

      #turn them into dataframes
      frames = [pd.read_excel(excel_name, ) for excel_name in excel_names]

      combined = pd.concat(frames, sort=False)

{% endhighlight %}

Check out the [GitHub][jekyll-github] for the full code. You can clone the repository and modify the code as per your requirement.

[jekyll-github]: https://github.com/akhilgeo/ExcelMerger/blob/master/excelmerger.py
