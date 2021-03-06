# Button Circle Control Plugin for Xamarin.Forms

Simple but elegant way of display circle buttons with an icon in your Xamarin.Forms projects. This project is based in [ImageCirclePlugin Project](https://github.com/jamesmontemagno/ImageCirclePlugin) developed by [James Montemagno](https://twitter.com/jamesmontemagno)

Build Status: [![Build status](https://ci.appveyor.com/api/projects/status/1yyib3ysj80mas1w?svg=true)](https://ci.appveyor.com/project/wilsonvargas/buttoncircleplugin)

#### Setup
* Available on NuGet: [![NuGet](https://img.shields.io/nuget/v/Plugins.Forms.ButtonCircle.svg?label=NuGet)](https://www.nuget.org/packages/Plugins.Forms.ButtonCircle/)
* Install into your PCL project and Client projects.

### Android

In your Android project call:

```
ButtonCircleRenderer.Init();
```
<img src="http://l7c.us/descargas/images/android.png" 
data-canonical-src="http://l7c.us/descargas/images/android.png"
 width="250" height="480" />

### iOS

In your iOS project call:

```
ButtonCircleRenderer.Init();
```

And add this key in your Info.plist

```
<key>UIAppFonts</key>
    <array>
      <string>MaterialIcons-Regular.ttf</string>
    </array>
```

You must do this AFTER you call Xamarin.Forms.Init();

**Platform Support**

|Platform|Supported|Version|
| ------------------- | :-----------: | :------------------: |
|Xamarin.iOS|Yes|iOS 7+|
|Xamarin.Android|Yes|API 14+|
|Windows Phone Silverlight|Is coming|
|Windows Phone RT|Is coming|
|Windows Store RT|Is coming|
|Windows 10 UWP|Is coming|
|Xamarin.Mac|No||

#### List of icons
You can see name of icons [here](https://github.com/wilsonvargas/ButtonCirclePlugin/blob/master/src/ButtonCircle/ButtonCircle.FormsPlugin.Abstractions/Icons.cs)

#### Usage
Instead of using an Button simply use a CircleButton instead!

You **MUST** set the width & height requests to the same value. Here is a sample:
```
new ButtonImage
{
  BorderColor = Color.Black,
  BorderThickness = 5,
  HeightRequest = 150,
  WidthRequest = 150,
  HorizontalOptions = LayoutOptions.Center,
  Icon = "ic_add"
}
```

**XAML:**

First add the xmlns namespace:
```xml
xmlns:local="clr-namespace:ButtonCircle.FormsPlugin.Abstractions;assembly=ButtonCircle.FormsPlugin.Abstractions"
```

Then add the xaml:

```xml
<local:CircleButton 
        Icon="ic_directions_bike" 
        FontSize="30" TextColor="Black" 
        HeightRequest="70" WidthRequest="70" 
        BorderThickness="5" BorderColor="Black" 
        BackgroundColor="#DCDCDC" Clicked="CircleButton_Clicked">
</local:CircleButton>
```

#### License
Licensed under MIT, see license file
