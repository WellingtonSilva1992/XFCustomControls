# XF Custom Controls

This library adds some non-existent functionality to controls such as ListView, Entry, Picker, and Slider.

```
Install-Package XFCustomControls 
```

```xml
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="XFCustomControls.Views.EntryExtView"
             xmlns:ext="clr-namespace:XFCustomControls.Ext;assembly=XFCustomControls.Ext"
             Title="XF Custom Controls"
             >
    <StackLayout Padding="40">
        <ext:Entry MaxLength="{Binding MaxLength}" Placeholder="MaxLength" Text="1234" />
        
        <ext:Slider ValueChangedCommand="{Binding ValueChangedCommand}" />
        
        <ext:Picker ItemsSource="{Binding Items}" 
                    SelectedItem="{Binding SelectedItem}"
                    SelectedItemChangedCommand="{Binding SelectedItemChangedCommand}" />
        
        <ext:ListView ItemsSource="{Binding Items}" 
                      ItemTappedCommand="{Binding ItemTappedCommand}"
                      InfiniteScrollCommand="{Binding InfiniteScrollCommand}"
                      >
            
        </ext:ListView>
    </StackLayout>    
</ContentPage>
```

# Entry
## MaxLength 
Bindable property which you can set a Max Length of Text in an Entry Control!

# Slider
## ValueChangedCommand 
Is fired when the Slider's Value is Changed

# Picker
## ItemsSource
Bindable property which you can set the items that will fill the picker!
You can use a ObservableCollection to add ou remove items dynamically.

## SelectedItem
Two Way Bindable property which you can set the selected item. 

## SelectedItemChangedCommand
Is fired when the Selected Item is Changed

# ListView
## ItemTappedCommand
Is fired when a listview item is tapped

## InfiniteScrollCommand
Is fired when a listview show the last item in the screen
