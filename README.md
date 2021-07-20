# It-Depends

`it-depends` produces the list of dependencies from a source code repository.
It-Depends currently supports Go, JavaScript, Rust, Python, and C/C++ projects.

## Quickstart 🚀

```commandline
$ pip3 install it-depends
```

### Running it 🏃
You simply point it to a repository:
```console
$ it-depends /path/to/project
```

It-Depends will output the full dependency hierarchy in JSON format. Additional output formats such
as Graphviz/Dot are available via the `--output-format` option.

Here is an example of running It-Depends on its own source repository:
![](https://gist.githubusercontent.com/feliam/e906ce723333b2b55237a71c4028559e/raw/e60f46c35b215a73a37a1d1ce3bb43eaead76af4/it-depends-demo.svg?sanitize=1)

This is the resulting [json](https://gist.github.com/feliam/2bdec76f7aa50602869059bfa14df156)
with all the discovered dependencies.
This is the resulting [Graphviz dot file](https://gist.github.com/feliam/275951f5788c23a477bc7cf758a32cc2)
producing this
![dependency graph](https://user-images.githubusercontent.com/1017522/116887041-33903b80-ac00-11eb-9288-f3d286231e47.png).
This is the [vis-network](https://github.com/visjs/vis-network) resulting graph.
![dependency graph](https://user-images.githubusercontent.com/1017522/126380710-0bf4fd66-0d2f-4cb1-a0ff-96fe715c4981.png).

### It-Depends’ Dependencies 🎭

JavaScript requires `npm`\
Rust requires `cargo`\
Python requires `pip`\
C/C++ requires `autotools` and/or `cmake`\
Several native dependencies are resolved using Ubuntu’s file to path database `apt-file`\
Currently `docker` is used to resolve native dependencies

## Development 👷
```commandline
$ git clone https://github.com/trailofbits/it-depends
$ cd it-depends
$ python3 -m venv venv  # Optional virtualenv
$ ./venv/bin/activate   # Optional virtualenv
$ pip3 install -e .[dev]
$ git config core.hooksPath ./hooks  # Optionally enable git commit hooks for linting
```

## License and Acknowledgements

This research was developed by [Trail of Bits](https://www.trailofbits.com/).
[Felipe Manzano](https://github.com/feliam) and [Evan Sultanik](https://github.com/ESultanik) are
the active maintainers, but [Alessandro Gario](https://github.com/alessandrogario),
[Eric Kilmer](https://github.com/ekilmer), and [Alexander Remie](https://github.com/rmi7) all made significant
contributions to the tool’s inception.
It-Depends is licensed under the [GNU Lesser General Public License v3.0](LICENSE).
[Contact us](mailto:opensource@trailofbits.com) if you’re looking for an exception to the terms.
© 2021, Trail of Bits.
