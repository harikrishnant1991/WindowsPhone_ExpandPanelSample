# ExpandPanel for Windows and Windows Phone
ExpandPanel is a control for Windows and Windows Phone 8.1+ that can be used to implement and expandable view.

## How to Use?

1. Include the `ExpandPanel.cs` file in your project.
2. In your applictaion's `Generic.xaml` file, include the namespace for `DrawerControl`, by adding this line:
``` XML
xmlns:jhp="using:JHControl.Panel"
```

So that the `ResourceDictionary` tag now looks like:

``` XML
<ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
                    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
                    xmlns:jhp="using:JHControl.Panel">
```

3. Now copy and paste the `ExpandPanel` style into your application's `Generic.xaml`.

4. In the `Page`/`UserControl` where you need to use the `ExpandPanel`, add the reference to the namespace and then add the following lines:

``` XML
<jhp:ExpandPanel HorizontalAlignment="Center"
                VerticalAlignment="Top"
                IsExpanded="False"
                Margin="25">
    <!--
    This is the header content of the ExpandPanel.
    On clicking on this, the expand panel expands.
    If this is not included, the header content won't show up and showing the content can only be done via code.
    You can customise the content as you like it.
    -->
    <jhp:ExpandPanel.HeaderContent>
        <Grid Height="50"
              Width="200"
              HorizontalAlignment="Stretch"
              VerticalAlignment="Stretch"
              Background="Red" />
    </jhp:ExpandPanel.HeaderContent>
    <!--
    This is the header content of the ExpandPanel, when expanded.
    On clicking on this, the expand panel collapses.
    If this is not included, the selected state header content won't show up and hiding the content can only be done via code.
    You can customise the content as you like it.
    -->
    <jhp:ExpandPanel.SelectedHeaderContent>
        <Grid Height="50"
              Width="200"
              HorizontalAlignment="Stretch"
              VerticalAlignment="Stretch"
              Background="Blue" />
    </jhp:ExpandPanel.SelectedHeaderContent>
    <!--
    The content of the ExpandPanel.
    If this is not implemented, the ExpandPanel won't expand.
    You can customise the content as you like it.
    -->
    <jhp:ExpandPanel.Content>
        <Grid Height="300"
              Width="200"
              Background="Green" />
    </jhp:ExpandPanel.Content>
</jhp:ExpandPanel>
```

1. The ExpandPanel has a `IsExpanded` property that can be used to expand and collapse the ExpandPanel as required.
2. The ExpandPanel has a `IsAnimationEnabled` property which can be used to specify if the expansion and collision should be animated or not.