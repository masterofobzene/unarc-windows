# unarc

The `unarc` is an unpacker for ArC archives (`"ArC\1"` header), that used in some installers with `.bin` suffix.
I've forked and used some LLM magic to make it possible to compile it on Windows without satanic rituals.
You can download the precompiled version from Releases now. 


Tested in Windows 10 X64 only.

## Motivation

- Original repo didn't give info on how to make it compilable on Windows.
- No precompiled release available.

## Usage
```
Usage: unarc command [options] archive[.arc] [filenames...]
Available commands:
  l - display archive listing
  v - display verbose archive listing
  e - extract files into current directory
  x - extract files with pathnames
  t - test archive integrity
Available options:
  -dp{Path}   - set destination path
  -w{Path}    - set temporary files directory
  -o+         - overwrite existing files
  -o-         - don't overwrite existing files
  --noarcext  - don't add default extension to archive name
  --          - no more options
```

## Building

- install mingw64 if you don't have it. Check that you have the corresponding environment variables.
- open a CMD and ````git clone https://github.com/xredor/unarc.git```` then ````cd unarc````
- then make the "build" directory inside (right click New->Folder or ````mkdir -p build````)
- run ````mkdir -p build````
