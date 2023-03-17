# anna-dl
Python tool allowing easy books downloads from the terminal

Replacement for [zlib-dl](https://github.com/Nquxii/zlib-dl)

<img src="images/demo-f.gif" align="center">

## Features 
- Bypass randomly generated links to downloads
- Obtain a specified number of results
- Retrieve metadata without having to go onto annas-archive.org itself

## Installation
Clone the repository and install dependencies
```
git clone https://github.com/Nquxii/anna-dl
cd anna-dl
```
```
pip3 install -r requirements.in
```

Open help section
```
python3 annadl --h
```

Ensure your config.json is set if you don't want to use several parameters each time.

Add annadl to path (so you don't need to cd into zlib-dl every time) Linux/MacOS:
```
ln -s ~[CURRENT DIR]/annadl ~/.local/bin/annadl
```

## Usage
```
python3 annadl [path] --s [query] --n [number of results]
```
Number of results defaults to 5 of the top results available. Use 0 to see all search results on the page.


If a path in the command is specified, it will be used. Otherwise, the download_path in config.json will be used.
If none of these options are available, the program will use `./assets/` as its download folder.

### Example
View 5 search results for "The Pragmatic Programmer". Download the resulting file in /home/johndoe/Documents/books
```
python3 annadl /home/johndoe/Documents/books --s "The Pragmatic Programmer"
```

View **all** search results on the first page for "Don Quixote". Download the resulting file in ./assets/ (assuming no set path in config.json)
```
python3 annadl --s "Don Quixote" --n 0
```
