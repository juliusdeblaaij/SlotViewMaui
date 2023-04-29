<img src="https://raw.githubusercontent.com/nor0x/SlotView.Maui/main/Art/icon.png" width="200px" />

# SlotView.Maui 🎰
[![.NET](https://github.com/nor0x/SlotView/actions/workflows/dotnet.yml/badge.svg)](https://github.com/nor0x/OverFlower/actions/workflows/dotnet.yml)
[![](https://img.shields.io/nuget/v/SlotView.Maui)](https://www.nuget.org/packages/SlotView.Maui)
[![](https://img.shields.io/nuget/dt/SlotView.Maui)](https://www.nuget.org/packages/SlotView.Maui)


<video width="100%" controls>
  <source src="https://raw.githubusercontent.com/nor0x/SlotView.Maui/main/Art/demo.mp4" type="video/mp4" />
</video>


a view that can animate images like a slot machine reel. Powered by Maui.Graphics and highly customizable.

## Installation
Add NuGet package to your project:
```
dotnet add package SlotView.Maui
```
or as PackageReference
```
<PackageReference Include="SlotView.Maui" Version="0.0.1" />
```

## Usage
```xml
xmlns:sv="clr-namespace:SlotView.Maui;assembly=SlotView.Maui"
...
<sv:SlotView
    x:Name="mySlotView"
    Speed="10"
    Drag="0.1"
    StopIndex="5"
    VisibleCount="3">
    <sv:SlotView.Images>
        <x:Array Type="{x:Type x:String}">
            <!-- images can be local or remote -->
            <x:String>myimg0.png</x:String>
            <x:String>https://foo.bar/myimg1.png</x:String>
            <x:String>myimg2.png</x:String>
            <x:String>https://foo.bar/myimg2.png</x:String>
        </x:Array>
    </sv:SlotView.Images>
</sv:SlotView>
```

or in code behind
```csharp
var mySlotView = new SlotView
{
    Speed = 10,
    Drag = 0.1f,
    StopIndex = 5,
    VisibleCount = 3,
    Images = new string[]
    {
        "myimg0.png",
        "https://foo.bar/myimg1.png",
        "myimg2.png",
        "https://foo.bar/myimg2.png"
    }
};
```

# SlotView Class Documentation

## Properties

### `BackgroundColor` property

**Type:** `Color`

**Description:** Gets or sets the background color of the control.

### `Images` property

**Type:** `string[]`

**Description:** Gets or sets the list of image paths to be displayed in the control.

### `Speed` property

**Type:** `float`

**Description:** Gets or sets the speed of the spinning animation.

### `MinimumSpeed` property

**Type:** `float`

**Description:** Gets or sets the minimum speed that the spinning animation can reach.

### `Drag` property

**Type:** `float`

**Description:** Gets or sets the drag of the spinning animation.

### `DragThreshold` property

**Type:** `int`

**Description:** Gets or sets the drag threshold of the spinning animation.

### `VisibleCount` property

**Type:** `int`

**Description:** Gets or sets the number of images to be displayed at once.

### `Delay` property

**Type:** `float`

**Description:** Gets or sets the delay before the spinning animation starts.

### `Duration` property

**Type:** `float`

**Description:** Gets or sets the duration of the spinning animation.

### `StopIndex` property

**Type:** `int`

**Description:** Gets or sets the index of the image to stop the spinning animation at.

### `IsSpinning` property

**Type:** `bool`

**Description:** Gets or sets a value indicating whether the spinning animation is currently running.

### `Direction` property

**Type:** `SlotDirection`

**Description:** Gets or sets the direction of the spinning animation.

## Events

### `ImagesLoaded` event

**Type:** `EventHandler`

**Description:** Occurs when the list of images has been loaded and is ready for display.

### `Started` event

**Type:** `EventHandler`

**Description:** Occurs when the spinning animation has started.

### `Paused` event

**Type:** `EventHandler`

**Description:** Occurs when the spinning animation has been paused.

### `Finished` event

**Type:** `EventHandler`

**Description:** Occurs when the spinning animation has finished.