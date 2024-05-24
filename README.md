# lintoptionsexample
Example repo showing lint options with the same name being overridden

## Reproducing

- Open project in Android Studio
- Build
- Open `TestClass.kt`
- Observe there is a lint error for `import nl.wykorijnsburger.featuremodule.R` with ID `MissingResourceImportAlias`
- Try to auto fix it (alt+enter on Mac)
- There is no auto-fix suggestion, even though `MissingResourceImportAlias` has setup the `import-aliases` option that should enable it
- Open `config/lint/lint.xml`
- Uncomment line 10
- Build
- Open `TestClass.kt`
- Try to auto fix the lint error again
- There is now an auto-fix suggestion
