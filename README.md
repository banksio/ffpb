# ffrich

**Not smart. Not comprehensive. Not guaranteed to work.**


`ffrich` is an FFmpeg progress formatter. It will attempt to display a
nice progress bar in the output, based on the raw `ffmpeg` output, as
well as an adaptative ETA timer.


## Usage

### On the command line

`ffrich` is is not self-aware. Any argument given to the `ffrich`
command is transparently given to the `ffmpeg` binary on
your system, without any form of validation.

```sh
ffrich <any_ffmpeg_command>
```

### Using as a library

`ffrich` can be used as a library: use the `ffrich.main`
function:

```python
ffrich.main(argv=None, stream=sys.stderr, encoding=None, console=rich.console.Console):
```

**argv**:   The arguments to pass to `ffmpeg`, as an argument list.

**stream**:   The stream to which to write the progress bar and the output
    messages.

**encoding**:   The encoding of the terminal, used to decode the `ffmpeg` output.
    Defaults to `locale.getpreferredencoding()`, or *UTF-8* is locales
    are not available.

**console**: The rich console object to output to.

## Installation

Install from PyPI:

```sh
pip install ffrich
```

Install from Git:

```sh
pip install git+https://github.com/banksio/ffrich.git
```
