# Label

**Inheritance:** [Element](https://docs.fabulous.dev/v2/api/controls/element/) -> [NavigableElement](https://docs.fabulous.dev/v2/api/navigable-element/) -> [VisualElement](https://docs.fabulous.dev/v2/api/visual-element/) -> [View](https://docs.fabulous.dev/v2/api/view/)\
**Xamarin.Forms documentation:** Label [API](https://docs.microsoft.com/en-us/dotnet/api/xamarin.forms.label) / [Guide](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/text/label)

For details on how the control actually works, please refer to the [Xamarin.Forms documentation](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/text/label).

### Constructors&#x20;

| Constructors        | Description                        |
| ------------------- | ---------------------------------- |
| Label(text: string) | Defines a Label widget with a text |

### Properties&#x20;

| Properties                                                                                  | Description                                                                                        |
| ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| characterSpacing(value: float)                                                              | Sets the spacing between each character of the text                                                |
| font(?size: float, ?namedSize: NamedSize, ?attributes: FontAttributes, ?fontFamily: string) | Sets the font                                                                                      |
| horizontalTextAlignment(value: textAlignment)                                               | Sets the horizontal alignment of the text                                                          |
| lineBreakMode(value: LineBreakMode)                                                         | Sets the line break mode                                                                           |
| lineHeight(value: float)                                                                    | Sets the multiplier to apply to the default line height when displaying text                       |
| maxLines(value: int)                                                                        | Sets the maximum number of lines allowed                                                           |
| padding(value: Thickness)                                                                   | Sets the amount of padding around the text                                                         |
| padding(value: float)                                                                       | Sets a uniform amount of padding around the text                                                   |
| padding(left: float, top: float, right: float, bottom: float)                               | Sets the amount of padding around the text                                                         |
| textColor(light: FabColor, ?dark: FabColor)                                                 | Sets the text color depending if light or dark mode                                                |
| textDecoration(value: TextDecorations)                                                      | Sets the text decorations (underline, strike, etc) to apply on the text                            |
| textTransform(value: TextTransform)                                                         | Sets the text transformation (lowercase, uppercase) to apply on the text                           |
| textType(value: TextType)                                                                   | Sets the text type (plain text, HTML)                                                              |
| verticalTextAlignment(value: TextAlignment)                                                 | Sets the vertical alignment of the text                                                            |
| reference(value: ViewRef\<Label>)                                                           | Sets a `ViewRef` instance to retrieve the `Xamarin.Forms.Label` instance associated to this widget |

### Shorthand properties&#x20;

| Properties             | Description                                                                                            |
| ---------------------- | ------------------------------------------------------------------------------------------------------ |
| centerTextHorizontal() | Center the text horizontally inside the Label. Same as `horizontalTextAlignment(TextAlignment.Center)` |
| centerTextVertical()   | Center the text vertically inside the Label. Same as `verticalTextAlignment(TextAlignment.Center)`     |

### Events&#x20;

None

### Usages&#x20;

```fsharp
Label("Hello World")
    .characterSpacing(1.)
    .font(namedSize = NamedSize.Large, fontFamily = "Arial", attributes = FontAttributes.Bold)
    .horizontalTextAlignment(TextAlignment.Center)
    .lineBreakMode(LineBreakMode.WordWrap)
    .lineHeight(1.5)
    .maxLines(1)
    .padding(10.)
    .textColor(light = Color.Red.ToFabColor(), dark = Color.Blue.ToFabColor())
    .textDecoration(TextDecorations.Underline)
    .textTransform(TextTransform.Lowercase)
    .textType(TextType.Text)
    .verticalTextAlignment(TextAlignment.Center)
```

#### Use shorthand properties&#x20;

```fsharp
Label("Hello World")
    .size(500., 500.)
    .centerTextHorizontal()
    .centerTextVertical()
```

#### Get access to the underlying Xamarin.Forms.Label&#x20;

```fsharp
let labelRef = ViewRef<Label>()

Label("Hello World")
    .reference(labelRef)
```
