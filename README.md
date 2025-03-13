# How-to-Create-Rounded-Rectangle-Radio-Buttons-and-Maintain-Group-Selection-in-.NET-MAUI
This repository contains a sample demonstrating how to create rounded rectangle RadioButtons and maintain group selection in .NET MAUI.

**Creating Rounded Rectangle Radio Buttons and Maintaining Group Selection in .NET MAUI.**

To create a rounded rectangle RadioButton, we need to place the RadioButton within a Border.To maintain group selection functionality, we use the RadioGroupKey.

The following code example illustrates  how to create rounded rectangle RadioButtons and ensure group selection is maintained in .NET MAUI.

**XAML**
```
<ContentPage.Resources>
    <Style x:Key="SettingsRoundRect" TargetType="Border">
        <Setter Property="WidthRequest" Value="300"/>
        <Setter Property="StrokeShape" Value="RoundRectangle 10"/>
    </Style>
</ContentPage.Resources>

<StackLayout>
  <buttons:SfRadioGroupKey x:Name="RadioGroupKey" Spacing="5" >
        <Border  Style="{StaticResource SettingsRoundRect}">
            <buttons:SfRadioButton Text="Style 1"  Value="1" GroupKey="{Binding Source={x:Reference RadioGroupKey}}"/>
        </Border>
      
        <Border Style="{StaticResource SettingsRoundRect}" >
            <buttons:SfRadioButton Text="Style 2" Value="2" GroupKey="{Binding Source={x:Reference RadioGroupKey}}"/>
        </Border>

        <Border Style="{StaticResource SettingsRoundRect}" >
            <buttons:SfRadioButton Text="Style 3" Value="3" GroupKey="{Binding Source={x:Reference RadioGroupKey}}"/>
        </Border>
    </buttons:SfRadioGroupKey>
</StackLayout>
```

**Path too long exception** 

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
