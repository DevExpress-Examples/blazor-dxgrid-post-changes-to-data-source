<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/522844306/23.1.3%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T1108021)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
# Grid for Blazor - How to post changes to an in-memory data source

When a user starts editing a row, our Blazor Grid ([DxGrid](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid)) creates an edit model - a copy of the processed data item. This model stores all changes while the original data item remains intact. You need to update the data source to save changes.

![Blazor DxGrid instantly update all fields of the processed data item](/images/update-all-fields.png)

The [EditModelSaving](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid.EditModelSaving) event fires when a user completes row edits and allows you to save changes. Use the event argument's [EditModel](https://docs.devexpress.com/Blazor/DevExpress.Blazor.GridEditModelSavingEventArgs.EditModel) property to access the edit model. The [DataItem](https://docs.devexpress.com/Blazor/DevExpress.Blazor.GridEditModelSavingEventArgs.DataItem) property allows you to access the proccessed data item as requirements dictate.

Use one of the following variants to save changes made in the edit model:

- Call the [CopyChangesToDataItem](https://docs.devexpress.com/Blazor/DevExpress.Blazor.GridEditModelSavingEventArgs.CopyChangesToDataItem) method.

- Install the [AutoMapper](https://github.com/AutoMapper/AutoMapper) library and call its `Map` method to assign all edit model field values to corresponding data item fields simultaneously.

## Files to Review

- [Index.razor](./CS/UpdateDataItemFields/Pages/Index.razor)

## Documentation

- [Grid: Bind to Data](https://docs.devexpress.com/Blazor/403737/grid/bind-to-data)
- [Grid: Edit Data and Validate Input](https://docs.devexpress.com/Blazor/403454/grid/edit-data-and-validate-input)

## More Examples

- [Blazor Grid - Inline Editing and Cell Edit Templates](https://github.com/DevExpress-Examples/blazor-grid-row-editing)
