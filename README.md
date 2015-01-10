# fatpack-simple example

Usage:

1. Install App::FatPacker::Simple

        > cpanm git://github.com/shoichikaji/App-FatPacker-Simple.git

2. To fatpack your `hello.pl`, first, install deps to `local` and `extlib`

        # install deps in cpanfile to local
        > carton install

        # install non core modules for old Perl to extlib
        > cpanm -nq --reinstall -Lextlib HTTP::Tiny parent

3. Now, fatpack!

        > fatpack-simple hello.pl
        # then get hello.fatpack.pl

## additional

The above steps can be wrapped up to `Daikufile`:

    > cpanm Daiku
    > daiku fatpack
