---
-api-id: M:Windows.UI.Xaml.Controls.SettingsFlyout.ShowIndependent
-api-type: winrt method
---

<!-- Method syntax
public void ShowIndependent()
-->

# Windows.UI.Xaml.Controls.SettingsFlyout.ShowIndependent

## -description
Opens the Settings flyout, and returns the user to the app after the flyout is dismissed.

## -remarks
If a [SettingsFlyout](settingsflyout.md) is shown by calling the [Show](settingsflyout_show_392493604.md) method, then clicking the Back button reopens the [SettingsPane](../windows.ui.applicationsettings/settingspane.md) after the [SettingsFlyout](settingsflyout.md) dismisses. If a [SettingsFlyout](settingsflyout.md) is shown by calling [ShowIndependent](settingsflyout_showindependent_61271159.md), then clicking the Back button dismisses the [SettingsFlyout](settingsflyout.md) and returns the user to the app; the [SettingsPane](../windows.ui.applicationsettings/settingspane.md) is not reopened.

Call the [ShowIndependent](settingsflyout_showindependent_61271159.md) method to open the [SettingsFlyout](settingsflyout.md) from a button in your app. In this case, because the user did not open the [SettingsFlyout](settingsflyout.md) from the [SettingsPane](../windows.ui.applicationsettings/settingspane.md), they should return to your app when they click the Back button.

Only one [SettingsFlyout](settingsflyout.md) is shown at a time. Calling [ShowIndependent](settingsflyout_showindependent_61271159.md) on a [SettingsFlyout](settingsflyout.md) closes any other [SettingsFlyout](settingsflyout.md) currently shown. The [SettingsFlyout](settingsflyout.md) being closed completes its close animation before the new [SettingsFlyout](settingsflyout.md) begins its show animation.

## -examples
This example shows how to use the [ShowIndependent](settingsflyout_showindependent_61271159.md) method to open a [SettingsFlyout](settingsflyout.md) from a button in your app.

```xaml
<Button Content="App update settings" Click="UpdateSettingsButton_Click"/>

```

```csharp
private void UpdateSettingsButton_Click(object sender, RoutedEventArgs e)
{
    UpdateSettingsFlyout updatesFlyout = new UpdateSettingsFlyout();
    updatesFlyout.ShowIndependent();
}
```

For more code in context, see Scenario 4 of the [App settings sample](https://go.microsoft.com/fwlink/p/?LinkID=310073) and [Quickstart: Add app help](https://msdn.microsoft.com/library/770b546b-c909-4ecb-8a1f-c2f6b3e573b7).

## -see-also
[Show](settingsflyout_show_392493604.md), [Quickstart: Add app settings](https://msdn.microsoft.com/library/9651582e-56bb-4e14-ae99-9d0ff8cae104), [Quickstart: Add app help](https://msdn.microsoft.com/library/770b546b-c909-4ecb-8a1f-c2f6b3e573b7)
