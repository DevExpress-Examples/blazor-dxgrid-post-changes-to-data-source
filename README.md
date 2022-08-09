# Grid for Blazor - How to instantly update all fields of the data item on saving

When a user starts editing a row, the [DxGrid](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid) creates an edit model - a copy of the processed data item. This model stores all changes, and the data item remains intact. You should copy the edit model's property values to the data item's properties to save changes. This example demonstrates how to use the [AutoMapper](https://github.com/AutoMapper/AutoMapper) library to instantly update all fields of the original data item.

![Blazor DxGrid instantly update all fields of the processed data item](~/images/update-all-fields.png)

The [EditModelSaving](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid.EditModelSaving) event occurs when a users completes editing a row. Use the event argument's [EditModel](https://docs.devexpress.com/Blazor/DevExpress.Blazor.GridEditModelSavingEventArgs.EditModel) property to access the edit model. The [DataItem](https://docs.devexpress.com/Blazor/DevExpress.Blazor.GridEditModelSavingEventArgs.DataItem) property allows you to access the proccessed data item.

## Files to Look At

- [Index.razor](./CS/UpdateDataItemFields/Pages/Index.razor)

## Documentation

- [Grid: Bind to Data](https://docs.devexpress.com/Blazor/403737/grid/bind-to-data)
- [Grid: Edit Data and Validate Input](https://docs.devexpress.com/Blazor/403454/grid/edit-data-and-validate-input)

## More Examples

- [Blazor Grid - Inline Editing and Cell Edit Templates](https://github.com/DevExpress-Examples/blazor-grid-row-editing)