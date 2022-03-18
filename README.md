# Organizing-larger-code-python

## Compressed files
Creating compress files for demos
```
- python -m demo_reader.compressed.bzipped test.bz2 data compressed with bz2
- python -m demo_reader.compressed.gzipped test.gz data compressed with gzip
```

Reading compress files examples
```
- python multi_reader_program test.bz2
- python multi_reader_program test.gz
```

## Namespace and Executable Packages

### Executable Zip files
Steps to make zip file executable:
```
- Creating zip file:
    - python -m zipfile -c multi_reader_program.zip multi_reader_program/*
        - python -m zipfile -c <zip file name> <contents to zip directory>
- Running zip file examples:
    - python multi_reader_program.zip test.bz2
    - python multi_reader_program.zip test.gz
```

### Executable Packages
#### **Executing directories vs Packages**
Executing a direcotry `python directory`:
- "directory" added to sys.path
- "directory/\_\_main\_\_.py" is not a package

Executing a package `python -m directory
- "directory" treaded as a package
- "directory/\_\_main\_\_.py" is a submodule of the directory package

#### **\_\_init\_\_.py vs \_\_main\_\_.py**
- \_\_init\_\_.py
    - Can execute any code it likes on import ...
- \_\_main\_\_.py
    - Only a package with \_\_main\_\_.py can be executed
