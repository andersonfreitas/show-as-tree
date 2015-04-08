# tree-view

Easily navigate a text file with the structure of the output of `find`.

```console
$ find . 
.
./Folder A
./Folder A/File A.txt
./Folder A/File B.txt
./Folder A/File C.txt
./Folder A/Folder
./Folder A/Folder/File A.txt
./Folder A/Folder/File B.txt
./Folder A/Folder/File C.txt
./Folder B/Folder
./Folder B/Folder/File A.txt
./Folder B/Folder/File B.txt
./Folder B/Folder/File C.txt
```

Then, using `tree-view`:

```console
$ find . | tree-view
```

You get:

![Screenshot](screenshot.png)

## Usage

```console
$ cat basictex-install.txt | tree-view
$ tree-view basictex-install.txt
```

## Use cases

Sometimes, it's useful for discovering which files are being installed by some script:

```console
$ find / > pre-install.txt
$ ./install.sh
$ find / > post-install.txt
$ diff pre-install.txt post-install.txt > diff.txt
$ awk # to replace '<', '>', and numeric positions
$ tree-view diff.txt
```

# Install

```sh
brew tap andersonfreitas/tree-view
brew install andersonfreitas/tree-view
```

