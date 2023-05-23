Module templatte.reportmodel.report_generator
=============================================

Classes
-------

`ReportGenerator(logo: pathlib.Path, style: pathlib.Path, template: reportmodel.template.Template = None)`
:   Generates reports in PDF format.
    
    Initialize the ReportGenerator object.
    
    Args:
        logo: The path to the logo file.
        style: The path to the CSS file.
        template: An optional Template object.

    ### Instance variables

    `formatters: list[typing.Callable[[dict], dict]]`
    :   Get the list of formatters.
        
        Returns:
            list: A list of formatter functions.

    `template`
    :   Get the template.
        
        Returns:
            Template: The template object.

    ### Methods

    `add_formatter(self, formatter: Callable[[dict], dict]) ‑> None`
    :   Add a formatter function to the list of formatters.
        
        Args:
            formatter: A function that takes a dictionary and returns a modified dictionary.

    `format(self, data: dict) ‑> dict`
    :   Apply the registered formatters to the data.
        
        Args:
            data: The data dictionary.
        
        Returns:
            dict: The formatted data dictionary.

    `generate(self, data: dict, path: str)`
    :   Generate a PDF report for the given data.
        
        Args:
            data: The data dictionary.
            path: The path to save the generated PDF.
        
        Returns:
            str: An error message if an error occurred, otherwise None.