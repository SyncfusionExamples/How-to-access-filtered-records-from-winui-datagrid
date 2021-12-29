# How to access filtered records from WinUI DataGrid?

## About the sample

This example describes how to access filtered records from WinUI DataGrid.

[SfDataGrid.View.Records](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Data.ICollectionViewAdv.html#Syncfusion_UI_Xaml_Data_ICollectionViewAdv_Filter) contains the records in the View, which displays the records visible to the user. To get the filtered records, you have to access the [SfDataGrid.View.Records](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Data.ICollectionViewAdv.html#Syncfusion_UI_Xaml_Data_ICollectionViewAdv_Filter) when the filter is applied. The [FilterChanged](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.SfDataGrid.html#Syncfusion_UI_Xaml_DataGrid_SfDataGrid_FilterChanged) event occurs whenever the filter is changed. Thus, by using this event, you can access the filtered records in [WinUI DataGrid](https://www.syncfusion.com/winui-controls/datagrid) (SfDataGrid). The following code example demonstrates how to get the filtered records by the [FilterChanged](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.DataGrid.SfDataGrid.html#Syncfusion_UI_Xaml_DataGrid_SfDataGrid_FilterChanged) event.

``` C#

this.dataGrid.FilterChanged += OnFilterChanged;

private void OnFilterChanged(object sender, Syncfusion.UI.Xaml.DataGrid.GridFilterEventArgs e)
{
     var filteredResult = this.dataGrid.View.Records.Select(recordentry => recordentry.Data);
}

```

The records in [SfDataGrid.View.Records](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Data.ICollectionViewAdv.html#Syncfusion_UI_Xaml_Data_ICollectionViewAdv_Filter) are of type [RecordEntry](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Data.RecordEntry.html) that contain the underlying data. Thus by taking the [recordentry.Data](https://help.syncfusion.com/cr/winui/Syncfusion.UI.Xaml.Data.RecordEntry.html#Syncfusion_UI_Xaml_Data_RecordEntry_Data), you can get the filtered records in the underlying type.

Take a moment to peruse the [WinUI DataGrid - Filtering](https://help.syncfusion.com/winui/datagrid/filtering) documentation, where you can find about filtering with code examples.

## Requirements to run the demo
Visual Studio 2019 and above versions
