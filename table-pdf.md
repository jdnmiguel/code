# Extract Tables from PDF 
I am using the camelot library, click [here](https://camelot-py.readthedocs.io/en/master/index.html) for more details.

1. Import the following libraries 

```
import camelot 
import ghostscript
import os 
import pandas as pd
```

2. Use camelot to read your pdf
```
my_pdf = camelot.read_pdf('mypath/table.pdf', pages='a-b') 
```
How to read the previous command? 
- `my_pdf` = the name of your output
- `camelot.read.pdf` = the function used to read your pdf 
- `'mypath/table.pdf'` = your pdf of interest
- `pages='a-b'` = extract tables from page a to b 

You can check whether it worked using by running `my_pdf'` it gives you the following output `<TableList n=13>` 

3. Export into an xlsx file
```
my_pdf.export('mypath/output.xlsx', f='excel', compress=False)
```
How to read the previous command? 
- `my_pdf` = the name of your previous camelot output 
- `export` = the function used to export your pdf into excel 
- `'mypath/output.xlsx'` = your newly created excel file 
- `f='excel'` = the format, here excel
- `compress=False` = turn it to True if you want to export multiple output into a .zip file
