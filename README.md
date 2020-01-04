# ad-resident_tracker

_A simple [AppDaemon](https://www.home-assistant.io/docs/ecosystem/appdaemon/) app to fire events when a `person` arrives/departs._

## App configuration

```yaml
resident_tracker:
  module: resident_tracker
  class: ResidentTracker
  residents:
    - person.wrboyce
    - person.mrs_wrboyce
```

key | optional | type | description
-- | -- | -- | -- 
`module` | False | string | The module name of the app.
`class` | False | string | The name of the Class.
`residents` | False | string[] | A list of person entities to track.


## Events

The following events will be emitted with the `person` who triggered the event:

* `resident_arrived`
* `house_became_occupied`
* `resident_departed`
* `house_became_vacant`
