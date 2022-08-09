<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/522844306/22.1.4%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T1108021)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
# Grid for Blazor - How to instantly update all fields of the data item on saving

When a user starts editing a row, the [DxGrid](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid) creates an edit model - a copy of the processed data item. This model stores all changes, and the data item remains intact. You should copy the edit model's property values to the data item's properties to save changes. This example demonstrates how to use the [AutoMapper](https://github.com/AutoMapper/AutoMapper) library to instantly update all fields of the original data item.

![Blazor DxGrid instantly update all fields of the processed data item](/images/update-all-fields.png)

The [EditModelSaving](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid.EditModelSaving) event occurs when a users completes editing a row. Use the event argument's [EditModel](https://docs.devexpress.com/Blazor/DevExpress.Blazor.GridEditModelSavingEventArgs.EditModel) property to access the edit model. The [DataItem](https://docs.devexpress.com/Blazor/DevExpress.Blazor.GridEditModelSavingEventArgs.DataItem) property allows you to access the proccessed data item.

## Files to Look At

- [Index.razor](./CS/UpdateDataItemFields/Pages/Index.razor)

## Documentation

- [Grid: Bind to Data](https://docs.devexpress.com/Blazor/403737/grid/bind-to-data)
- [Grid: Edit Data and Validate Input](https://docs.devexpress.com/Blazor/403454/grid/edit-data-and-validate-input)

## More Examples

- [Blazor Grid - Inline Editing and Cell Edit Templates](https://github.com/DevExpress-Examples/blazor-grid-row-editing)
