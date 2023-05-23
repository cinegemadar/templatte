Module templatte.datamodel.data_source
======================================

Classes
-------

`CsvDataSource()`
:   Data source for CSV files.
    
    Initialize the CSV data source.

    ### Ancestors (in MRO)

    * templatte.datamodel.data_source.IDataSource
    * abc.ABC

    ### Methods

    `connect(self, connection: str, csv_params: dict = None) ‑> None`
    :   Connect to the CSV file.

`ExcelDataSource(connection: str, excel_args: dict)`
:   Data source for Excel files.
    
    Initialize the Excel data source.

    ### Ancestors (in MRO)

    * templatte.datamodel.data_source.IDataSource
    * abc.ABC

    ### Methods

    `connect(self) ‑> None`
    :   Connect to the Excel file.

`IDataSource()`
:   Interface for data sources.
    
    Initialize the data source.

    ### Ancestors (in MRO)

    * abc.ABC

    ### Descendants

    * templatte.datamodel.data_source.CsvDataSource
    * templatte.datamodel.data_source.ExcelDataSource

    ### Instance variables

    `data: dict`
    :   Get the transformed data.

    ### Methods

    `add_transformer(self, transformer: Callable[[pandas.core.frame.DataFrame], pandas.core.frame.DataFrame]) ‑> None`
    :   Add a data transformer.

    `connect(self) ‑> None`
    :   Connect to the data source.

    `transform(self)`
    :   Transform the data using registered transformers.