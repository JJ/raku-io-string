# IO::String [![Test in a Raku container](https://github.com/JJ/raku-io-string/actions/workflows/test.yaml/badge.svg)](https://github.com/JJ/raku-io-string/actions/workflows/test.yaml)

*This is a fork of the original
[IO::String](https://github.com/hoelzro/p6-io-string), which was archived, with
the intention of maintaining and releasing it again into the ecosystem*

## SYNOPSIS

```raku
        use IO::String;

        my $buffer = IO::String.new;
        {
            my $*OUT = $buffer;
            say "hello";
        }
        say ~$buffer; # hello
```


## DESCRIPTION

Sometimes you want to use code that deals with files (or other file-like
objects), but you don't want to mess around with creating temporary files. This
includes uses like APIs that for some reason don't accept strings as well as
files as targets, mocking I/O, or capturing output written to the
terminal. That's why this module exists. Loosely based on Perl 5's IO::String.

## TODO

  * Handle encodings

## LICENSE


(c) `hoelzro`, 2017. Released under the MIT [license](LICENSE)
