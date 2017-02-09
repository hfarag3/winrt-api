---
-api-id: T:Windows.UI.Xaml.Media.BitmapCache
-api-type: winrt class
---

<!-- Class syntax.
public class BitmapCache : Windows.UI.Xaml.Media.CacheMode, Windows.UI.Xaml.Media.IBitmapCache
-->

# Windows.UI.Xaml.Media.BitmapCache

## -description
Represents the behavior of caching a visual element or tree of elements as bitmap surfaces.

## -remarks
This class is infrastructure, and provides the underlying run-time value for the behavior when you specify `CacheMode="BitmapCache"` in XAML markup, or create a new [BitmapCache](bitmapcache.md) in code to set [UIElement.CacheMode](../windows.ui.xaml/uielement_cachemode.md).

## -examples
Use any of these syntax forms to set [UIElement.CacheMode](../windows.ui.xaml/uielement_cachemode.md) to a value other than the **null** default. Don't do this routinely without testing first, see "Remarks" in [UIElement.CacheMode](../windows.ui.xaml/uielement_cachemode.md).

```xaml
<Canvas CacheMode="BitmapCache">
  ...
</Canvas>
```

```csharp
canvas1.CacheMode = new BitmapCache(); //canvas1 is an existing named element in UI
```

```cpp
canvas1->CacheMode = ref new BitmapCache(); //canvas1 is an existing named element in UI
```



## -see-also
[UIElement.CacheMode](../windows.ui.xaml/uielement_cachemode.md), [IsOverdrawHeatMapEnabled](../windows.ui.xaml/debugsettings_isoverdrawheatmapenabled.md), [Optimize your XAML markup](http://msdn.microsoft.com/library/569e8c27-fa01-41d8-80b9-1e3e637d5b99)