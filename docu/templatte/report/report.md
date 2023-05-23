Module templatte.report.report
==============================

Classes
-------

`Report(data_model: datamodel.data_source.IDataSource, report_model: reportmodel.report_generator.ReportGenerator)`
:   Generates reports using a data source and report generator.
    
    Initialize the Report object.
    
    Args:
        data_model: An instance of a data source implementing the IDataSource interface.
        report_model: An instance of a report generator.

    ### Methods

    `create(self, path: Callable[[dict], str])`
    :   Create reports using the provided data source and report generator.
        
        Args:
            path: A callable that returns the path for each generated report, based on the provided data.