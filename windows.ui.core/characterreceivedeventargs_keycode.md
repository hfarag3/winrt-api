---
-api-id: P:Windows.UI.Core.CharacterReceivedEventArgs.KeyCode
-api-type: winrt property
---

<!-- Property syntax
public uint KeyCode { get; }
-->

# Windows.UI.Core.CharacterReceivedEventArgs.KeyCode

## -description
Gets the key code of the character whose input raised the event.

## -property-value
The key code of the character received by the input queue.

## -remarks
> **Windows 10**
> Apps do not receive this event when an [](http://msdn.microsoft.com/library/5fcc73e6-f499-47e6-8e81-0014ca4d241c) is enabled. The Input Method Editor (IME) handles all keyboard input and sets [Handled](characterreceivedeventargs_handled.md) to **true**.

> **Windows Phone**
> This API is supported in native apps only.

## -examples

## -see-also
[CharacterReceived](corewindow_characterreceived.md)