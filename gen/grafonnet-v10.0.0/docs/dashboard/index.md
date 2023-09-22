# dashboard

grafonnet.dashboard

## Subpackages

* [annotation](annotation.md)
* [link](link.md)
* [variable](variable.md)

## Index

* [`fn new(title)`](#fn-new)
* [`fn withAnnotations(value)`](#fn-withannotations)
* [`fn withAnnotationsMixin(value)`](#fn-withannotationsmixin)
* [`fn withDescription(value)`](#fn-withdescription)
* [`fn withEditable(value=true)`](#fn-witheditable)
* [`fn withFiscalYearStartMonth(value=0)`](#fn-withfiscalyearstartmonth)
* [`fn withLinks(value)`](#fn-withlinks)
* [`fn withLinksMixin(value)`](#fn-withlinksmixin)
* [`fn withLiveNow(value=true)`](#fn-withlivenow)
* [`fn withPanels(value)`](#fn-withpanels)
* [`fn withPanelsMixin(value)`](#fn-withpanelsmixin)
* [`fn withRefresh(value)`](#fn-withrefresh)
* [`fn withRefreshMixin(value)`](#fn-withrefreshmixin)
* [`fn withSchemaVersion(value=36)`](#fn-withschemaversion)
* [`fn withStyle(value="dark")`](#fn-withstyle)
* [`fn withTags(value)`](#fn-withtags)
* [`fn withTagsMixin(value)`](#fn-withtagsmixin)
* [`fn withTemplating(value)`](#fn-withtemplating)
* [`fn withTemplatingMixin(value)`](#fn-withtemplatingmixin)
* [`fn withTimezone(value="browser")`](#fn-withtimezone)
* [`fn withTitle(value)`](#fn-withtitle)
* [`fn withUid(value)`](#fn-withuid)
* [`fn withVariables(value)`](#fn-withvariables)
* [`fn withVariablesMixin(value)`](#fn-withvariablesmixin)
* [`fn withWeekStart(value)`](#fn-withweekstart)
* [`obj graphTooltip`](#obj-graphtooltip)
  * [`fn withSharedCrosshair()`](#fn-graphtooltipwithsharedcrosshair)
  * [`fn withSharedTooltip()`](#fn-graphtooltipwithsharedtooltip)
* [`obj time`](#obj-time)
  * [`fn withFrom(value="now-6h")`](#fn-timewithfrom)
  * [`fn withTo(value="now")`](#fn-timewithto)
* [`obj timepicker`](#obj-timepicker)
  * [`fn withCollapse(value=true)`](#fn-timepickerwithcollapse)
  * [`fn withEnable(value=true)`](#fn-timepickerwithenable)
  * [`fn withHidden(value=true)`](#fn-timepickerwithhidden)
  * [`fn withRefreshIntervals(value=["5s","10s","30s","1m","5m","15m","30m","1h","2h","1d"])`](#fn-timepickerwithrefreshintervals)
  * [`fn withRefreshIntervalsMixin(value=["5s","10s","30s","1m","5m","15m","30m","1h","2h","1d"])`](#fn-timepickerwithrefreshintervalsmixin)
  * [`fn withTimeOptions(value=["5m","15m","1h","6h","12h","24h","2d","7d","30d"])`](#fn-timepickerwithtimeoptions)
  * [`fn withTimeOptionsMixin(value=["5m","15m","1h","6h","12h","24h","2d","7d","30d"])`](#fn-timepickerwithtimeoptionsmixin)

## Fields

### fn new

```jsonnet
new(title)
```

Creates a new dashboard with a title.

### fn withAnnotations

```jsonnet
withAnnotations(value)
```

`withAnnotations` adds an array of annotations to a dashboard.

This function appends passed data to existing values


### fn withAnnotationsMixin

```jsonnet
withAnnotationsMixin(value)
```

`withAnnotationsMixin` adds an array of annotations to a dashboard.

This function appends passed data to existing values


### fn withDescription

```jsonnet
withDescription(value)
```

Description of dashboard.

### fn withEditable

```jsonnet
withEditable(value=true)
```

Whether a dashboard is editable or not.

### fn withFiscalYearStartMonth

```jsonnet
withFiscalYearStartMonth(value=0)
```

The month that the fiscal year starts on.  0 = January, 11 = December

### fn withLinks

```jsonnet
withLinks(value)
```

Dashboard links are displayed at the top of the dashboard, these can either link to other dashboards or to external URLs.

`withLinks` takes an array of [link objects](./link.md).

The [docs](https://grafana.com/docs/grafana/latest/dashboards/build-dashboards/manage-dashboard-links/#dashboard-links) give a more comprehensive description.

Example:

```jsonnet
local g = import 'g.libsonnet';
local link = g.dashboard.link;

g.dashboard.new('Title dashboard')
+ g.dashboard.withLinks([
  link.link.new('My title', 'https://wikipedia.org/'),
])
```


### fn withLinksMixin

```jsonnet
withLinksMixin(value)
```

Dashboard links are displayed at the top of the dashboard, these can either link to other dashboards or to external URLs.

`withLinks` takes an array of [link objects](./link.md).

The [docs](https://grafana.com/docs/grafana/latest/dashboards/build-dashboards/manage-dashboard-links/#dashboard-links) give a more comprehensive description.

Example:

```jsonnet
local g = import 'g.libsonnet';
local link = g.dashboard.link;

g.dashboard.new('Title dashboard')
+ g.dashboard.withLinks([
  link.link.new('My title', 'https://wikipedia.org/'),
])
```


### fn withLiveNow

```jsonnet
withLiveNow(value=true)
```

When set to true, the dashboard will redraw panels at an interval matching the pixel width.
This will keep data "moving left" regardless of the query refresh rate.  This setting helps
avoid dashboards presenting stale live data

### fn withPanels

```jsonnet
withPanels(value)
```



### fn withPanelsMixin

```jsonnet
withPanelsMixin(value)
```



### fn withRefresh

```jsonnet
withRefresh(value)
```

Refresh rate of dashboard. Represented via interval string, e.g. "5s", "1m", "1h", "1d".

### fn withRefreshMixin

```jsonnet
withRefreshMixin(value)
```

Refresh rate of dashboard. Represented via interval string, e.g. "5s", "1m", "1h", "1d".

### fn withSchemaVersion

```jsonnet
withSchemaVersion(value=36)
```

Version of the JSON schema, incremented each time a Grafana update brings
changes to said schema.
TODO this is the existing schema numbering system. It will be replaced by Thema's themaVersion

### fn withStyle

```jsonnet
withStyle(value="dark")
```

Theme of dashboard.

Accepted values for `value` are "dark", "light"

### fn withTags

```jsonnet
withTags(value)
```

Tags associated with dashboard.

### fn withTagsMixin

```jsonnet
withTagsMixin(value)
```

Tags associated with dashboard.

### fn withTemplating

```jsonnet
withTemplating(value)
```

TODO docs

### fn withTemplatingMixin

```jsonnet
withTemplatingMixin(value)
```

TODO docs

### fn withTimezone

```jsonnet
withTimezone(value="browser")
```

Timezone of dashboard. Accepts IANA TZDB zone ID or "browser" or "utc".

### fn withTitle

```jsonnet
withTitle(value)
```

Title of dashboard.

### fn withUid

```jsonnet
withUid(value)
```

Unique dashboard identifier that can be generated by anyone. string (8-40)

### fn withVariables

```jsonnet
withVariables(value)
```

`withVariables` adds an array of variables to a dashboard


### fn withVariablesMixin

```jsonnet
withVariablesMixin(value)
```

`withVariablesMixin` adds an array of variables to a dashboard.

This function appends passed data to existing values


### fn withWeekStart

```jsonnet
withWeekStart(value)
```

TODO docs

### obj graphTooltip


#### fn graphTooltip.withSharedCrosshair

```jsonnet
withSharedCrosshair()
```

Share crosshair on all panels.

#### fn graphTooltip.withSharedTooltip

```jsonnet
withSharedTooltip()
```

Share crosshair and tooltip on all panels.

### obj time


#### fn time.withFrom

```jsonnet
withFrom(value="now-6h")
```



#### fn time.withTo

```jsonnet
withTo(value="now")
```



### obj timepicker


#### fn timepicker.withCollapse

```jsonnet
withCollapse(value=true)
```

Whether timepicker is collapsed or not.

#### fn timepicker.withEnable

```jsonnet
withEnable(value=true)
```

Whether timepicker is enabled or not.

#### fn timepicker.withHidden

```jsonnet
withHidden(value=true)
```

Whether timepicker is visible or not.

#### fn timepicker.withRefreshIntervals

```jsonnet
withRefreshIntervals(value=["5s","10s","30s","1m","5m","15m","30m","1h","2h","1d"])
```

Selectable intervals for auto-refresh.

#### fn timepicker.withRefreshIntervalsMixin

```jsonnet
withRefreshIntervalsMixin(value=["5s","10s","30s","1m","5m","15m","30m","1h","2h","1d"])
```

Selectable intervals for auto-refresh.

#### fn timepicker.withTimeOptions

```jsonnet
withTimeOptions(value=["5m","15m","1h","6h","12h","24h","2d","7d","30d"])
```

TODO docs

#### fn timepicker.withTimeOptionsMixin

```jsonnet
withTimeOptionsMixin(value=["5m","15m","1h","6h","12h","24h","2d","7d","30d"])
```

TODO docs