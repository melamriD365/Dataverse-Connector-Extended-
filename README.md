# Dataverse Connector (Extended)
This custom connector implements triggers for Power Automate Cloud Flows that are not supported by the Dataverse connector. The custom connector supports the following triggers: 
- When an activity is updated

This list can be expanded to include other triggers.  

#### Custom trigger 1: When an activity is updated
This trigger allows you to execute a Cloud Flow when any activity type entity changes.

- Trigger Configuration: 
  - query parameter to monitor state change: **$filter**
  - value to pass to selected query parameter: **(modifiedon ne createdon and modifiedon gt @{triggerBody().value[0].modifiedon})**
  - collection that contains trigger data: **@triggerBody().value**

More details on my blog: https://xrmtricks.com/2021/09/06/implementing-triggers-for-power-automate-flows-that-are-not-supported-by-the-dataverse-connector/

