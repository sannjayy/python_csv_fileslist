## CSV Files List Generator from Folders with Subfolders
GitHub Repo: [https://github.com/sannjayy/python_export_file_info](https://github.com/sannjayy/python_export_file_info)
### Installaion

`pip install python-export-file-info`

**Import:**
```
from csv_filelist_generator import FileListGenerator
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
| **monitor** | *False* | True / False |Show Process Bar on Terminal
| **filename** | exported_list.csv | *any* **.csv** | CSV Output Filename.

- After the name **.csv** extension is required.

- Default Output Folder: **output/** *[In Project Root]*

---

**Full Code Example:**
```
from python_export_file_info import FileListGenerator

scan_folder_path = r"C:\Users\sannjayy\Desktop"
myfolder = FileListGenerator(scan_folder_path)
myfolder.filter_extensions = ('.mp4', '.mp3') 
myfolder.generate(monitor=True, filename='pyfiles.csv')
```

To Filter Files by Extensions [*Optional*]: `folder.filter_extensions = ('.mp4', '.mp3', '.jpg')`.

**DEMO OUTPUT:**

Here is the exported demo file structure.

| Name | Extention | Size | Directory | Created Date | Modified Date | CRC32 *(hash)* | SH1 *(hash)* | MD5 *(hash)* |
| --------- | --------- | ---- | --------- | -----------  | ----|--|--|--|
| myfile | .mp3| 3.5MB | /dir/sub/ | 2022-05-29 13:33:10.058800 | 2022-06-19 17:00:01.871203 | 362C499D | 8dcdb80bbf5b0e430f6982588e2aaf07f1b3b01b | 1a7178a8438f5a45bbdb1bc416df0ec3

---

[![](https://img.shields.io/github/followers/sannjayy?style=social)](https://github.com/sannjayy)  
Developed by *Sanjay Sikdar*.   
- 📫 hello@znas.in



