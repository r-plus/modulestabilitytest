# Module stability reproducible project.

# How to reproduce issue

1. xcode-select to 11.1

```
$ sudo xcode-select -s /Applications/Xcode11.1.app/Contents/Developer
```

2. build Eureka framework by Carthage with config.xcconfig to support module stay

```
$ XCODE_XCCONFIG_FILE=$(pwd)/config.xcconfig carthage bootstrap --platform iOS
```

3. build this project on Xcode 11.2, errors will appear.

- Failed to load module 'Eureka'
- Unknown attribute '_staticInitializeObjCMetadata'
- Redundant conformance of 'AreaRow\<Cell\>' to protocol 'FormatterConformance'
