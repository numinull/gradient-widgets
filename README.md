# Gradient widgets

Little gradient widgets for the web, with Melbourne weather, time and calendar views.

## The collection

| Widget | What it does | Open it | Source |
| --- | --- | --- | --- |
| Melbourne Widget Stack | Combined clock, weather and calendar panels | [Widget stack](https://numinull.github.io/gradient-widgets/melbourne_widget_stack.html) | [melbourne_widget_stack.html](melbourne_widget_stack.html) |
| Calendar | Standalone calendar with event and observance information | [Calendar](https://numinull.github.io/gradient-widgets/calendar.html) | [calendar.html](calendar.html) |
| Weather navigation | Compact Melbourne time and weather bar | [Weather bar](https://numinull.github.io/gradient-widgets/nav-weather.html) | [nav-weather.html](nav-weather.html) |
| Dark weather navigation | Dark variant of the weather bar | [Dark weather bar](https://numinull.github.io/gradient-widgets/nav-weather-black.html) | [nav-weather-black.html](nav-weather-black.html) |

The `moon-icons/` and `weather-icons/` folders contain supporting image assets.

## Use a widget

Open a widget using the links above. To add it to Notion, copy its URL, type `/embed`, paste the link and resize the block.

Use the individual HTML links rather than the site's root address. There is no gallery `index.html` in this collection.

## Run locally

```sh
git clone https://github.com/numinull/gradient-widgets.git
cd gradient-widgets
python3 -m http.server 8000
```

With Python 3 installed, open [localhost:8000](http://localhost:8000/) and choose an HTML file. Keep the server running while previewing; press Ctrl+C to stop it. There is no package installation or build step.

## Dependencies and customisation

The pages load React, ReactDOM and Babel from external CDNs, and fonts from Google Fonts. Weather widgets request Melbourne weather from Open-Meteo. An internet connection is needed for those dependencies and live data.

The widget stack and navigation bars use different weather requests and dependency versions. A page loading successfully does not guarantee that every weather field is available.

Styles and scripts are embedded in each HTML file. To customise a widget, edit its file and keep the relative asset paths intact. Changing the weather location requires reviewing the coordinates, displayed place name and time-zone handling together.

Some event information is written directly into the source, including dated entries in the widget stack. Review it when maintaining the calendar rather than assuming all events update automatically.

## Maintaining the collection

- Keep existing filenames and published URLs stable for embedded widgets.
- Check both weather-bar variants when changing shared behaviour.
- Check weather loading, calendar navigation and narrow embed layouts after changes.
- Add any new widget to the table above.

The separate [Notion widgets collection](https://github.com/numinull/notion_widgets) contains sticky notes, a mini calendar, a daily panel and a KaTeX designer.
