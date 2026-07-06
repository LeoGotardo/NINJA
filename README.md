# NINJA

A small Python utility script for reading and inspecting raw binary data from a file, chunk by chunk, and dumping the results as hex.

## What it does

`Test.py` opens a binary file, seeks to a given byte offset, and reads a series of fixed-size chunks. For each chunk it:

- Prints the hex representation to the console
- Appends the hex representation to `output.txt`
- Shows progress via a progress bar (`alive_progress`)

By default it targets `C:\Outlive\outlive.dat` starting at offset `43644082`, reading `10` chunks of `200` bytes each. Adjust `file_path`, `offset`, `chunk_size`, and `total_chunks` in `Test.py` as needed for your own file.

## Requirements

- Python 3
- [`alive-progress`](https://pypi.org/project/alive-progress/)

Install dependencies:

```bash
pip install alive-progress
```

## Usage

```bash
python Test.py
```

Output is printed to the console and appended to `output.txt` in the working directory.
