---
-api-id: T:Windows.UI.Xaml.EventTrigger
-api-type: winrt class
---

<!-- Class syntax.
public class EventTrigger : Windows.UI.Xaml.TriggerBase, Windows.UI.Xaml.IEventTrigger
-->

# Windows.UI.Xaml.EventTrigger

## -description
Represents a trigger that applies a set of actions (animation storyboards) in response to an event. Not commonly used. See Remarks.

## -xaml-syntax
```xaml
<EventTrigger>
  oneOrMoreBeginStoryboards
</EventTrigger>
 
```


## -remarks
[Triggers](frameworkelement_triggers.md), [EventTrigger](eventtrigger.md), [Actions](eventtrigger_actions.md) and [BeginStoryboard](../windows.ui.xaml.media.animation/beginstoryboard.md) are not commonly used. These API mainly exist for compatibility in XAML originally used for Microsoft Silverlight. For most scenarios where event triggers were used previously, do one of these:
+ Use built-in animations from the animation library. See [Quickstart: Animating your UI using the animation library](http://msdn.microsoft.com/library/4e715281-d247-4e7f-9f88-2af0d88ed5cf).
+ For events in control templates, use visual states and [VisualStateManager](visualstatemanager.md). See [Storyboarded animations for visual states](http://msdn.microsoft.com/library/5e715281-d247-4e7f-9f88-2af0d88ed5e4) or [Quickstart: Control templates](http://msdn.microsoft.com/library/67c424ae-afb1-4560-a6a8-4a3506775d77).
+ For app-specific UI animations, define a [Loaded](frameworkelement_loaded.md) handler on the page. This handler can reference a [Storyboard](visualstate_storyboard.md) that's defined in page-level resources, and call the [Begin](../windows.ui.xaml.media.animation/storyboard_begin.md) method on that [Storyboard](../windows.ui.xaml.media.animation/storyboard.md). See [Storyboarded animations](http://msdn.microsoft.com/library/0cbceea0-2b0e-44a1-a09a-f7a939632f3a).


If you do choose to use [Triggers](frameworkelement_triggers.md), in Windows Runtime XAML, the default behavior for event triggers and the only event that can be used to invoke an [EventTrigger](eventtrigger.md) is [FrameworkElement.Loaded](frameworkelement_loaded.md). Because that's both the default and the only enabled behavior, don't set the [RoutedEvent](eventtrigger_routedevent.md) attribute. Just use the XAML `<EventTrigger>`. If you set [RoutedEvent](eventtrigger_routedevent.md) explicitly (not recommended), the only XAML that works is `<EventTrigger RoutedEvent="FrameworkElement.Loaded">`. Unqualified "Loaded", or any other value, throws a parse exception. For more info, see [Triggers](frameworkelement_triggers.md).

## -examples
This XAML example shows the basic structure for using [FrameworkElement.Triggers](frameworkelement_triggers.md) with its default [FrameworkElement.Loaded](frameworkelement_loaded.md) trigger behavior to run a storyboarded animation. This XAML shows the [EventTrigger](eventtrigger.md) and [BeginStoryboard](../windows.ui.xaml.media.animation/beginstoryboard.md) container elements in proper relationship with each using their XAML content property syntax and unnecessary property element tags omitted.

```xaml
<Canvas Width="200" Height="200" x:Name="animatedcanvas" Background="Red">
    <Canvas.Triggers>
        <EventTrigger>
            <BeginStoryboard>
                <Storyboard x:Name="ColorStoryboard">
                   <!-- Animate the background of the canvas to green over 4 seconds. -->
                    <ColorAnimation Storyboard.TargetName="animatedcanvas"
                      Storyboard.TargetProperty="(Panel.Background).(SolidColorBrush.Color)"
                      To="Green" Duration="0:0:4"/>
                </Storyboard>
            </BeginStoryboard>
        </EventTrigger>
    </Canvas.Triggers>
</Canvas>
```



## -see-also
[TriggerBase](triggerbase.md), [Triggers](frameworkelement_triggers.md), [Storyboarded animations for visual states](http://msdn.microsoft.com/library/5e715281-d247-4e7f-9f88-2af0d88ed5e4), [Quickstart: Control templates](http://msdn.microsoft.com/library/67c424ae-afb1-4560-a6a8-4a3506775d77)