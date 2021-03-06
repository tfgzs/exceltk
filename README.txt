# Convert Excel sheet to MarkDown Table
  - HyperLink cell in Excel sheet will be **retained** as `[text](url)` format 
  - CrossLine cell in Excel sheet will be **expanded** to multirow
  - Empty columns on the right side will be **trimed**, which is **detected** by the first 100 rows. 
  - Support set the precision of decimal
  - Support to set markdown table aligin
  - Convert newline in cell text into `<br/>`
  - Cross sheet Hyperlink formula support, link formula like `HYPERLINK(test_sheet!C9,...)` will be extract as `[text](url)` format automatic
  - Hyperlink formula support, link formula like `HYPERLINK(C9,...)` will be extract as `[text](url)` format automatic

### Useage:
  
  if in MacOS, just replace the `exceltk.exe` with `exceltk`

  - `exceltk.exe -t md -xls example.xls` 
  - `exceltk.exe -t md -xls example.xls -sheet sheetname`
  - `exceltk.exe -t md -xls example.xlsx` 
  - `exceltk.exe -t md -xls example.xlsx -sheet sheetname`
  - `exceltk.exe -t md -p 2 -xls example.xls`, where `-p 2` setting the decimal precision to 2
  - `exceltk.exe -t md -bhead -xls example.xls`, which will use the first row to replace table header, and keep the head empty, so that 
  the table will auto response in small screen device, this is just a simply solution.
  - `exceltk.exe -t cm`, Now you can copy sheet from excel, then paster to any editor, which will be Markdown table.
  - `exceltk -t md -a r -xls example.xlsx`, where the `-a` option can be followd by a aligin character
    - `-a l`: aligin left
    - `-a r`: aligin right
    - `-a c`: aligin center

# Convert Excel to Json 
  chagne the `-t` option to `json`
  - `exceltk.exe -t json -xls example.xls `

# Convert Excel to TeX
  change the `-t` option to `tex`
  - `exceltk.exe -t tex -xls example.xls`
  - using `-st n` option to split table into multitable
  - using `-sn` option to adjust number, for example, `1234656` will be split into `1 2 3 4 5 6`, it the table width is too large, this is useful
