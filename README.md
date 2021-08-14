pub

## Description

A CupertinoRangeSlider for Flutter.

## Example

```dart
    import 'package:cupertino_range_slider/cupertino_range_slider.dart';
    import 'package:flutter/material.dart';

    void main() {
        runApp(MyApp());
    }

    class MyApp extends StatelessWidget {
        @override
        Widget build(BuildContext context) {
            return MaterialApp(
                title: 'Flutter Demo',
                theme: ThemeData(
                    primarySwatch: Colors.blue,
                ),
                home: MyHomePage(title: 'Flutter Demo Home Page'),
            );
        }
    }

    class MyHomePage extends StatefulWidget {
    MyHomePage({Key? key, required this.title}) : super(key: key);

    final String title;

    @override
    _MyHomePageState createState() => _MyHomePageState();
    }

    class _MyHomePageState extends State<MyHomePage> {

    RangeValues _value = RangeValues(0.0, 1.0);

    void _reset() {
        setState(() {
        _value = RangeValues(0.0, 1.0);
        });
    }

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            appBar: AppBar(
                title: Text(widget.title),
            ),
            body: Center(
                child: CupertinoRangeSlider(
                    min: 0.0,
                    max: 20.0,
                    values: _value,
                    onChanged: (RangeValues value) {
                        setState(() {
                            _value = value;
                        });
                    },
                ),
            ),
            floatingActionButton: FloatingActionButton(
                onPressed: _reset,
                tooltip: 'Reset',
                child: Icon(Icons.restore),
            ),
        );
    }
}

```

## Installation

To Install the package add the following line to your pubspec.yaml file:

```yaml
    dependencies:
        cupertino_range_slider: ^0.0.1
```

Run `flutter pub get` and you should be good to go.

## Usage

This package can be used just as the `RangeSlider` widget that came out of the box with Flutter is used.
The above example demonstrates the use of the `cupertino_range_slider` package.