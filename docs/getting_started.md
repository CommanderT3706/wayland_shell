# Getting Started

Here is a simple guide to installing and using `wayland_shell`

## Installation

At this time of writing, `wayland_shell` is not available on pub.dev. It is recommended to install from GitHub temporarily. Add the following under `dependencies` in your `pubspec.yaml`:
```yaml
wayland_shell:
  git:
    url: https://github.com/FlafyDev/wayland_shell.git
    rev: main
```

## Using the library

Ensure the package is imported to your `main.dart` file:
```dart
import 'package:wayland_shell/wayland_shell.dart'
```

Initialize the library in your `main.dart`:
```dart
void main() async {
  WidgetsFlutterBinding.ensureInitialized(); // Ensure Flutter is initialized

  await WaylandShell.init(
    namespace: "wayland_shell_example_statusbar", // Used for application to be identified by the compositor
  );

  runApp(const MyApp());
}
```

The above code ensures Flutter is initialized, and there after initializes the wayland_shell library.
