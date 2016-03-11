# line-macro
Line Macro will read the input file line by line and handle macroinstruction.

## Usage
```sh
line-macro  INPUT_FILE_PATH  [OUTPUT_FILE_PATH]

INPUT_FILE_PATH         Path of input file

OUTPUT_FILE_PATH        Path of output file
                        It will be overwrited if file exists. If not given, output to stdout insteads.
```

## Syntax
Each macroinstruction should start from the beginning of the line. Only empty spaces or tabs are accepted before the macroinstruction, Otherwise, the line will be considered as a normal line.

Normal lines will be sent to output directly without any changes.

#### ~import
Import external file from the FILE_PATH and replace the current line. The macroinstruction in the external file will be handled recursively.
```sh
~import  FILE_PATH ;
```

## Error
Line Macro will stop for any error occurs.
