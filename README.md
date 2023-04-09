## Scaffold for developing Sui smart contracts in Move

```
a_move_package
├── Move.toml      (required)
├── sources        (required)
├── examples       (optional, test & dev mode)
├── scripts        (optional)
├── doc_templates  (optional)
└── tests          (optional, test mode)
```

Directories marked required must be present in order for the directory to be considered a Move package and to be compiled. Optional directories can be present, and if so will be included in the compilation process. Depending on the mode that the package is built with (test or dev), the tests and examples directories will be included as well.

The sources directory can contain both Move modules and Move scripts (both transaction scripts and modules containing script functions). The examples directory can hold additional code to be used only for development and/or tutorial purposes that will not be included when compiled outside test or dev mode.

A scripts directory is supported so transaction scripts can be separated from modules if that is desired by the package author. The scripts directory will always be included for compilation if it is present. Documentation will be built using any documentation templates present in the doc_templates directory.
