# How to access filtered records from WinUI DataGrid?

## About the sample

This example describes how to access filtered records from WinUI DataGrid.

In [WinUI DataGrid](https://www.syncfusion.com/winui-controls/datagrid) (SfDataGrid), the records visible to the user were present in the [SfDataGrid.View.Records](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Data.ICollectionViewAdv.html#Syncfusion_UI_Xaml_Data_ICollectionViewAdv_Filter) property. When the filter is applied, the SfDataGrid.View.Records property can be used to get the filtered records. The [FilterChanged](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.SfDataGrid.html#Syncfusion_UI_Xaml_DataGrid_SfDataGrid_FilterChanged) event occurs whenever the filter is changed. Thus, by using this event, the filtered records can be accessed in DataGrid. The following code example demonstrates how to get the filtered records by the FilterChanged event.

``` C#

this.dataGrid.FilterChanged += OnFilterChanged;

private void OnFilterChanged(object sender, Syncfusion.UI.Xaml.DataGrid.GridFilterEventArgs e)
{
     var filteredResult = this.dataGrid.View.Records.Select(recordEntry => recordEntry.Data);
}

```

The records in SfDataGrid.View.Records are of type [RecordEntry](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Data.RecordEntry.html) that contain the underlying data. Thus by taking the [recordentry.Data](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Data.RecordEntry.html#Syncfusion_UI_Xaml_Data_RecordEntry_Data), the filtered records can be accessed in the underlying type.

Take a moment to peruse the [WinUI DataGrid - Filtering](https://help.syncfusion.com/winui/datagrid/filtering) documentation, where you can find about filtering with code examples.

## Requirements to run the demo
Visual Studio 2019 and above versions
