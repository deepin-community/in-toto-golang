## in-toto record start

Creates a preliminary link file recording the paths and hashes of the
passed materials and signs it with the passed functionary’s key.

### Synopsis

Creates a preliminary link file recording the paths and hashes of the
passed materials and signs it with the passed functionary’s key.
The resulting link file is stored as ‘.<name>.<keyid prefix>.link-unfinished’.

```
in-toto record start [flags]
```

### Options

```
  -h, --help                    help for start
  -m, --materials stringArray   Paths to files or directories, whose paths and hashes
                                are stored in the resulting link metadata before the
                                command is executed. Symlinks are followed.
```

### Options inherited from parent commands

```
  -c, --cert string                       Path to a PEM formatted certificate that corresponds
                                          with the provided key.
  -e, --exclude stringArray               Path patterns to match paths that should not be recorded as 
                                          ‘materials’ or ‘products’. Passed patterns override patterns defined
                                          in environment variables or config files. See Config docs for details.
      --follow-symlink-dirs               Follow symlinked directories to their targets. Note: this parameter
                                          toggles following linked directories only, linked files are always
                                          recorded independently of this parameter.
  -k, --key string                        Path to a private key file to sign the resulting link metadata.
                                          The keyid prefix is used as an infix for the link metadata filename,
                                          i.e. ‘<name>.<keyid prefix>.link’. See ‘–key-type’ for available
                                          formats. Passing one of ‘–key’ or ‘–gpg’ is required.
  -l, --lstrip-paths stringArray          Path prefixes used to left-strip artifact paths before storing
                                          them to the resulting link metadata. If multiple prefixes
                                          are specified, only a single prefix can match the path of
                                          any artifact and that is then left-stripped. All prefixes
                                          are checked to ensure none of them are a left substring
                                          of another.
  -d, --metadata-directory string         Directory to store link metadata (default "./")
  -n, --name string                       Name for the resulting link metadata file.
                                          It is also used to associate the link with a step defined
                                          in an in-toto layout.
      --normalize-line-endings            Enable line normalization in order to support different
                                          operating systems. It is done by replacing all line separators
                                          with a new line character.
      --spiffe-workload-api-path string   UDS path for SPIFFE workload API
      --use-dsse                          Create metadata using DSSE instead of the legacy signature wrapper.
```

### SEE ALSO

* [in-toto record](in-toto_record.md)	 - Creates a signed link metadata file in two steps, in order to provide
              evidence for supply chain steps that cannot be carried out by a single command

