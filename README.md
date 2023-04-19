# fill

This is a Python script that utilizes the [ROOT](https://root.cern) library to draw histograms from data in a file. It supports 1D and 2D histograms, and provides options to customize binning, axis ranges, and data delimiters.

Requirements

- Python 3.x
- [ROOT](https://root.cern) library for Python

## Usage

```sh
python3 -i fill [options] data_file

```

## Positional arguments

`data_file`: Path to the input data file.

## Optional arguments

- `-x`, `--xcol`: Target column number for the x-axis (default: 0).
- `--xbins`: Number of bins for the x-axis (default: 100).
- `--xmin`: Minimum value for the x-axis (must be a string expression).
- `--xmax`: Maximum value for the x-axis (must be a string expression).
- `-y`, `--ycol`: Target column number for the y-axis.
- `--ybins`: Number of bins for the y-axis (default: 100).
- `--ymin`: Minimum value for the y-axis (must be a string expression).
- `--ymax`: Maximum value for the y-axis (must be a string expression).
- `--dlm`: Data delimiter used in the data file (default: None).
- `--cmt`: Comment delimiter used in the data file (default: "#").

## Examples

### Plot a 1D histogram using all values in a file:

```sh
python3 -i fill data.txt

```

### Plot a 1D histogram using values from a specific column:

```sh
python3 -i fill --xcol 2 data.txt
```

### Plot a 2D histogram using values from two specific columns:

```sh
python3 -i fill --xcol 1 --ycol 2 data.txt
```

### Customize binning and axis range:

```sh
python3 -i fill --xcol 1 --xbins 50 --xmin "0" --xmax "100" data.txt
```

### Specify data delimiter and comment delimiter:

```sh
python3 -i fill --xcol 1 --dlm "," --cmt "#" data.txt
```

## Notes

- The script assumes that the data file is formatted with columns separated by the specified delimiter, and comments are denoted by the specified comment delimiter.
- The input file can contain any number of rows, but the data must be properly formatted to be read by the script.
- The script will generate a canvas with the histogram and wait for a `Ctrl-C` input on the canvas to exit.

<!--
## Features

## Reference
-->

## Author
 [yoshphys](https://github.com/yoshphys)

## Licence
 fill is under MIT license. See the [LICENSE](https://github.com/yoshphys/dot2pdf/blob/main/LICENSE) for more info.
