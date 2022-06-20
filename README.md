## CSV File Info List Generator from Folders and Subfolders
Export files information from directory and subdirectory with process monitor. 

Currently only **.csv** format supported for output/export.

GitHub Repo: [https://github.com/sannjayy/python_export_file_info](https://github.com/sannjayy/python_export_file_info)
### Installaion
Do the following in your virtualenv:

`pip install python-export-file-info`

**Import:**
```
from python_export_file_info import FileListGenerator
```
---
**Minimal Code Example:**
```
from python_export_file_info import FileListGenerator

myfolder = FileListGenerator(folder='/home/')
myfolder.generate()
```

---


**Generate Options:**

| Syntax | Default | Options | Description |
| ------- | ------- | ------------ |  ------------------ |
| **monitor** | False | True / False |Show process bar on terminal. |
| **filename** | exported_list.csv | *any* **.csv** | Output CSV Filename.|
| **index** | True | True / False | Add ID column.|
| **file_prefix** | None | *any* | Prefix of `file` column.|
| **remove_non_ascii** | False | True / False | Remove Non ASCII Characters from File Name |

- `remove_non_ascii` may unable to find your files.
- /dir/myfile.mp3 > `file_prefix='new/sub/'` > new/sub/dir/myfile.mp3
- Default Output Folder: **output/** *[In Project Root]*.

---

**Full Code Example:**
```
from python_export_file_info import FileListGenerator

scan_folder_path = r"C:\Users\sannjayy\Desktop"
myfolder = FileListGenerator(folder=scan_folder_path, output_path='newpath/')
myfolder.filter_extensions = ('.mp4', '.mp3') 
myfolder.generate(monitor=True, filename='pyfiles.csv')
```

- To Filter Files by Extensions [*Optional*]: `folder.filter_extensions = ('.mp4', '.mp3', '.jpg')`.

- To change the default output path  use `output_path='newpath/'`

---

**DEMO OUTPUT:**

Exported demo csv file structure.

| ID | Name | Extention | Size | File | CRC32 *(hash)* | SH1 *(hash)* | MD5 *(hash)* | Modified Date | Created Date |
| -- | ---- | --------- | ---- | ---- | -------------- | ------------ | ------------ | ------------- | ------------ |
| 1 | myfile | .mp3 | 4.29 MB | /dir/myfile.mp3 | 362... | 8dcdb... | 1a717... | 2022-06-19 13:33:12 | 2022-05-19 10:45:12 |

---

[![](https://img.shields.io/github/followers/sannjayy?style=social)](https://github.com/sannjayy)  
Developed by *Sanjay Sikdar*.   
- 📫 hello@znas.in



