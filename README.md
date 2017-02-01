# WP REST API Sidebars V2
An extension for the WP REST API that exposes endpoints for sidebars and widgets.

*note: this plugin is based on WP REST API Sidebars V1.*

## Installation

Install directly from within wp-admin. Or get the files from either this repo or from the official [WP REST API Sidebars V2][] plugin to the plugin directory and activate the plugin.

note: to enable you to use any version/branch of the [WP REST API][] plugin during this rapid development phase there is currently no good way to check if it is active. Therefore make sure that it is before you activate this plugin.

[WP REST API]: https://wordpress.org/plugins/rest-api
[WP REST API Sidebars]: https://wordpress.org/plugins/wp-rest-api-sidebars-v2

## Currently supported endpoints
**/wp-json/wp-rest-api-sidebars/v2/sidebars** *returns a list of registered sidebars*

```json
[
    {
        "name": "Sidebar Name",
        "id": "sidebar-id",
        "description": "Sidebar description...",
        "class": "sidebar-class",
        "before_widget": "<aside id=\"%1$s\" class=\"widget %2$s\">",
        "after_widget": "<\/aside>",
        "before_title": "<h1 class=\"widget-title\">",
        "after_title": "<\/h1>"
    }
]
```

**/wp-json/wp-rest-api-sidebars/v1/sidebars/{id}** *returns the given sidebar*

```json
{
    "name": "Sidebar Name",
    "id": "sidebar-id",
    "description": "Sidebar description...",
    "class": "sidebar-class",
    "before_widget": "<aside id=\"%1$s\" class=\"widget %2$s\">",
    "after_widget": "<\/aside>",
    "before_title": "<h1 class=\"widget-title\">",
    "after_title": "<\/h1>",
    "rendered": "<aside id=\"widget-id-1\" class=\"widget widget_widget-id\">...",
    "widgets": [
        {
            "name": "Widget Name",
            "id": "widget-name-1",
            "classname": "widget_widget_name",
            "description": "Widget description",
            "rendered": "<aside id=\"widget-names-1\" class=\"widget widget_widget_name\">..."
        }
    ]
}
```
