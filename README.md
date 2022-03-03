# jupyter-notebook-tools

This repository contains several `nbconvert templates` to convert jupyter notebook (.ipynb) file into **HTML format**. These templates offer multiple ways to hide code blocks in jupyter notebook. The converted html examples can be found under `converted_html_examples/` folder. All templates were modified based on `classic` HTML template which is provided in nbconvert core for the HTML exporter.

Additional information on creating `custom tempaltes for nbconvert` can be found [HERE](https://nbconvert.readthedocs.io/en/latest/customizing.html)

*Note*: These templates have been tested with Python3.7 and 3.8

## How to
- Assuming that both **jupyter notebook and nbconvert** have been installed successfully, copy the contents of `converted_html_examples/` folder to the local template location. Or, you can add `--TemplateExporter.extra_template_basedirs` argument in the command line which allows you to point to the location of templates.

- Run the command line blow
```
jupyter nbconvert <PAHT_TO_IPYNB> --to html --no-prompt --template <TEMPLATE_NAME> --TemplateExporter.extra_template_basedirs <TEMPLATES_FOLDER> --output <OUTPUT_HTML_BASENAME>
```
A real example using the notebook inside this repo would be 
```
jupyter nbconvert test_new_code_toggle.ipynb --to html --no-prompt --template classic_add_toggle_each_cell --TemplateExporter.extra_template_basedirs nbconvert_templates/ --output test_html
```
