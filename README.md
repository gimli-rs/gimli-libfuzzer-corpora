# gimli-libfuzzer-corpora

`libFuzzer` corpora for `gimli`'s fuzz targets.

For each of `gimli`'s fuzz targets, there is a directory in this repository
containing that fuzz target's corpus.

## Using These Corpora

First, install `cargo fuzz`:

```
$ cargo install cargo-fuzz
```

Next, clone this repo into the path `fuzz/corpus` within your `gimli` checkout:

```
$ cd path/to/gimli
$ git clone https://github.com/gimli-rs/gimli-libfuzzer-corpora.git fuzz/corpus
```

Finally, run a fuzz target, e.g. the `eh_frame` fuzz target:

```
$ cargo fuzz run eh_frame
```

## Minimizing a Corpus

After you've set up your `gimli` checkout to use this repo as described above:

```
$ cd path/to/gimli
$ cargo fuzz cmin <target>
```
