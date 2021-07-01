# how to set outer border for flutter datatable

The Syncfusion Flutter DataTable widget provides support to set the border i.e grid lines by using following properties,

•	SfDataGrid.gridLinesVisibility: To set the grid lines for the cells other than header and stacked header cells.

•	SfDataGrid.headerGridLinesVisibility: To set the grid lines of header and stacked header cells.

## Set grid lines for data cells

By default, DataGrid shows horizontal grid lines. The following example shows how to set vertical and horizontal grid lines. 

```xml
@override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Syncfusion Flutter DataGrid'),
      ),
      body: SfDataGrid(
        source: employeeDataSource,
        gridLinesVisibility: GridLinesVisibility.both,
        headerGridLinesVisibility: GridLinesVisibility.both,
        columnWidthMode: ColumnWidthMode.fill,
        columns: <GridColumn>[
          GridColumn(
              columnName: 'id',
              label: Container(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  alignment: Alignment.center,
                  child: Text(
                    'ID',
                  ))),
         GridColumn(
              columnName: 'name',
              label: Container(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  alignment: Alignment.center,
                  child: Text('Name'))),
          GridColumn(
              columnName: 'designation',
              label: Container(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  alignment: Alignment.center,
                  child: Text(
                    'Designation',
                    overflow: TextOverflow.ellipsis,
                  ))),
          GridColumn(
              columnName: 'salary',
              label: Container(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  alignment: Alignment.center,
                  child: Text('Salary'))),
        ],
      ),
    );
  }
```
<img alt="data cells grid lines "  src="https://www.syncfusion.com/uploads/user/kb/flut/flut-4299/flut-4299_img1.png" width="300" height="400" />
## Set grid lines for header cells

By default, DataGrid shows horizontal grid lines. The following example shows how to set vertical and horizontal grid lines to header cells. 
```xml
@override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Syncfusion Flutter DataGrid'),
      ),
      body: SfDataGrid(
        source: employeeDataSource,
        gridLinesVisibility: GridLinesVisibility.both,
        headerGridLinesVisibility: GridLinesVisibility.both,
        columnWidthMode: ColumnWidthMode.fill,
        columns: <GridColumn>[
          GridTextColumn(
              columnName: 'id',
              label: Container(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  alignment: Alignment.center,
                  child: Text(
                    'ID',
                  ))),
          GridTextColumn(
              columnName: 'name',
              label: Container(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  alignment: Alignment.center,
                  child: Text('Name'))),
          GridTextColumn(
              columnName: 'designation',
              label: Container(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  alignment: Alignment.center,
                  child: Text(
                    'Designation',
                    overflow: TextOverflow.ellipsis,
                  ))),
          GridTextColumn(
              columnName: 'salary',
              label: Container(
                  padding: EdgeInsets.symmetric(horizontal: 16.0),
                  alignment: Alignment.center,
                  child: Text('Salary'))),
        ],
      ),
    );
  }
```
 <img alt="header cells grid lines "  src="https://www.syncfusion.com/uploads/user/kb/flut/flut-4299/flut-4299_img2.jpeg" width="300" height="400" />

## Set outer border for DataGrid

By default, the top and bottom border for datagrid will be shown. To show another border i.e. left and right, you can wrap the SfDataGrid inside the Container and set the required borders for container.

```xml
@override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Syncfusion Flutter DataGrid'),
      ),
      body: Container(
        decoration: BoxDecoration(
            border: Border(
                right:
                    BorderSide(width: 1, color: Color.fromRGBO(0, 0, 0, 0.26)),
                bottom:
                    BorderSide(width: 1, color: Color.fromRGBO(0, 0, 0, 0.26)),
                left: BorderSide(
                    width: 1, color: Color.fromRGBO(0, 0, 0, 0.26)))),        
     child: SfDataGrid(
          source: employeeDataSource,
          columnWidthMode: ColumnWidthMode.fill,
          columns: <GridColumn>[
            GridTextColumn(
                columnName: 'id',
                label: Container(
                    padding: EdgeInsets.symmetric(horizontal: 16.0),
                    alignment: Alignment.center,
                    child: Text(
                      'ID',
                    ))),
            GridTextColumn(
                columnName: 'name',
                label: Container(
                    padding: EdgeInsets.symmetric(horizontal: 16.0),
                    alignment: Alignment.center,
                    child: Text('Name'))),
            GridTextColumn(
                columnName: 'designation',
                label: Container(
                    padding: EdgeInsets.symmetric(horizontal: 16.0),
                    alignment: Alignment.center,
                    child: Text(
                      'Designation',
                      overflow: TextOverflow.ellipsis,
                    ))),
            GridTextColumn(
                columnName: 'salary',
                label: Container(
                    padding: EdgeInsets.symmetric(horizontal: 16.0),
                    alignment: Alignment.center,
                    child: Text('Salary'))),
          ],
        ),
      ),
    );
  }
```
<img alt="Datatable outer border "  src="https://www.syncfusion.com/uploads/user/kb/flut/flut-4299/flut-4299_img3.png" width="300" height="400" />
 
**[View document in Syncfusion Flutter Knowledge base](https://www.syncfusion.com/kb/12522/how-to-set-border-for-flutter-datatable-sfdatagrid)**

