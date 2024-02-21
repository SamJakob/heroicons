# HeroIcons

[heroicons](https://heroicons.com/) port to Flutter. This package renders the icons as SVG
images.

<!-- start:heroicons_version -->
  <!-- 
  DO NOT MODIFY: This section is automatically generated by
  'tool/fetch_icons.dart'
  -->

  This package was last updated to use [heroicons](https://heroicons.com/)
  version [`2.1.1`](https://github.com/tailwindlabs/heroicons/releases/tag/v2.1.1)
  (on `February 21st, 2024`). If there's a newer version of HeroIcons available, please
  create an issue or pull request.

<!-- end:heroicons_version -->

## Usage

```dart
class MyExampleWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return HeroIcon(
      HeroIcons.calendar,
      style: HeroIconStyle.outline, // Outlined icons are used by default.
      color: Colors.red,
      size: 30,
    );
  }
}
```

You can also use `HeroIconTheme` to set the default style (e.g., outline or solid) for all icons in your app.
(You'll still be able to override the style for individual icons.)

```dart
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      // ...
      home: HeroIconTheme(
        style: HeroIconStyle.solid,
        child: MyHomePage(),
      ),
    );
  }
}
```

## Install

Add `heroicons` package into your `pubspec.yaml`.

```yaml
dependencies:
  heroicons: # Latest version
```

You can also run `flutter pub add heroicons` to quickly add latest version from your CLI.

## Development

Fetch new icons and automatically generate source code for `heroicons.dart` (runs both of the below steps)

```
dart tool/update.dart
```

### Extra Commands

If, for any reason, you need to run the steps separately, you can do so as follows:

- Fetch new icons, organize into `assets/` and update the README.
  ```bash
  dart tool/fetch_icons.dart
  ```
  
  Optionally, a branch may be specified to fetch icons from. For example, to fetch icons from the `dev` branch:
  ```bash
  dart tool/fetch_icons.dart dev
  ```
  
  Note that older branches (i.e., `v1`) won't work yet as the SVGs are organized differently and not all styles are
  available.


- Run source code generation to create `heroicons.dart` file with an enum entry for every icon.
  ```bash
  dart tool/generator.dart
  ```
