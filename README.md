# Overlay On Widget

[![pub package](https://img.shields.io/pub/v/overlay_on_widget.svg)](https://pub.dev/packages/overlay_on_widget)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

A Flutter package for adding overlay widgets on top of other widgets with ease.

![Overlay On Widget](https://github.com/EngrMonyrul/package_image/blob/main/Screenshot_20230904_184407%5B1%5D.jpg)
![Overlay On Widget](https://github.com/EngrMonyrul/package_image/blob/main/OverlayOnWidget.png)

## Features

- Easily overlay widgets on top of other widgets.
- Supports customizable positioning and dimensions of overlay widgets.
- Ideal for creating tooltips, pop-ups, or any overlay UI elements.
- Provides a simple and convenient API for adding and managing overlays.

## Installation

1. Add this to your `pubspec.yaml`:
```yaml
dependencies:
  overlay_on_widget: ^0.0.2 # Use the latest version from pub.dev
```

2. Install the package by running:
```shell
flutter pub get
```

3. Import the package in your code:
```dart
import 'package:overlay_on_widget/overlay_on_widget.dart';
```

4. Add package:
```shell
dart pub add overlay_on_widget
```

Usage:
Overlaying a Widget
To overlay a widget on top of another widget, you can use the OverlayOnWidget widget. 
Here's an example:
```dart
Container(
  decoration: ShapeDecoration(
  color: Colors.blue,
  shape: CustomCutoutShapeBorder(
    CutoutScreenArea(
      borderColor: Colors.red,
      borderWidth: 3.0,
      overlayColor: Color.fromRGBO(0, 0, 0, 80),
      borderRadius: 10.0,
      borderLength: 40.0,
      cutOutWidth: 150.0,
      cutOutHeight: 150.0,
      ),
    ),
  ),
),
```

Example:
```dart
import 'package:flutter/material.dart';

import 'cutoutscreen.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: Stack(
            alignment: Alignment.center,
            children: [
              Image.network(
                'https://images.pexels.com/photos/2739666/pexels-photo-2739666.jpeg?cs=srgb&dl=pexels-tom-fisk-2739666.jpg&fm=jpg',
                fit: BoxFit.cover,
              ),
              Positioned.fill(
                child: Container(
                  decoration: ShapeDecoration(
                    color: Colors.blue,
                    shape: OverlayOnWidget(
                      CutoutScreenArea(
                        borderColor: Colors.red,
                        borderWidth: 3.0,
                        overlayColor: Color.fromRGBO(0, 0, 0, 80),
                        borderRadius: 10.0,
                        borderLength: 40.0,
                        cutOutWidth: 150.0,
                        cutOutHeight: 150.0,
                      ),
                    ),
                  ),
                ),
              )
            ],
          ),
        ),
      ),
    );
  }
}
```

Changelog:
See the Changelog file for detailed changes and version history.

Roadmap:
Add support for customizing overlay on any widget.
Enhance overlay positioning options.
Provide additional examples and use cases.

Issues and Feedback:
Please report any issues or provide feedback on GitHub Issues.

Contributing:
Contributions are welcome! Follow the Contributing Guide to get started.

License:
This package is open-source and available under the MIT License.

Author:
Monirul Islam (+8801729602502 - WhatsApp)

GitHub:
https://github.com/EngrMonyrul

Support:
For any inquiries or support, you can reach out to [engrmonirulislam513@gmail.com].
