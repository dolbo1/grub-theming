# extract

Extracting files from archives is a pretty simple task.

Most archives you'll come across, including GRUB themes, will be of the .tar.gz format.

`tar` is a very powerful archiving command-line tool, with tons of options, but for the sake of simplicity I'll just cover extraction.

To extract all of the files from an archive, here called `example.tar.gz`, you'll use the following command:

    $ tar -xf example.tar.gz

This command will extract all files stored in the archive to the current directory.

If you want to extract all of the files into a specific folder, here called `ExampleFiles`, run the following:

    $ mkdir ExampleFiles
    $ mkdir tar -xf example.tar.gz -C ExampleFiles

Now all of the extracted files will be found in `ExampleFiles`.
