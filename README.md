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