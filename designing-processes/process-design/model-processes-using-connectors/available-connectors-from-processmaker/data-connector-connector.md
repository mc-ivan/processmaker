---
description: >-
  Access both ProcessMaker Collection records and third-party data sources from
  Process models, then make workflow routing decisons based on that data.
---

# Data Connector Connector

## Overview

The [Data Connector](../../../data-connector-management/what-is-a-data-connector.md) connector is part of the [Data Connector package](../../../../package-development-distribution/package-a-connector/data-connector-package.md). From the Data Connector connector, select a [ProcessMaker Data Connector](../../../data-connector-management/what-is-a-data-connector.md) from which to interact with a data source.

Use the Data Connector connector in your Process models in the following ways:

* **Access ProcessMaker Collections:** From your [Process model](../../what-is-process-modeling.md), interact with any [ProcessMaker Collection](../../../../collections/what-is-a-collection.md) in your ProcessMaker instance, including viewing, creating, updating, and/or delete records in a selected Collection. By default, each ProcessMaker Collection has a corresponding Data Connector when it is created. Incorporate ProcessMaker Collection record data into your Process model so you can make business decisions using it. Likewise, automatically change records in a ProcessMaker Collection during a [Request](../../../../using-processmaker/requests/what-is-a-request.md) when workflow routing conditions are met.
* **Access third-party data sources:** Similarly to ProcessMaker Collections, interact with third-party data sources such as Application Program Interfaces \(APIs\). Reference data from that API, then incorporate it into your Process's Request data. Incorporating data from external data sources helps you make business decisions from information outside of your ProcessMaker instance.

{% hint style="info" %}
### ProcessMaker Package Required

The Data Connector connector requires that the [Data Connector package](../../../../package-development-distribution/package-a-connector/data-connector-package.md) be installed in your ProcessMaker instance. The Data Connector connector and the Data Connector [package](../../../../package-development-distribution/first-topic.md) are not available in the ProcessMaker open-source edition. Contact [ProcessMaker Sales](https://www.processmaker.com/contact/) or ask your ProcessMaker sales representative how the Data Connector connector can be installed in your ProcessMaker instance.
{% endhint %}

## Add a Data Connector Connector to the Process Model

{% hint style="info" %}
### ProcessMaker Package Required

The [Data Connector package](../../../../package-development-distribution/package-a-connector/data-connector-package.md) is required. The Data Connector [package](../../../../package-development-distribution/first-topic.md) installs the Data Connector connector, which is not available in the ProcessMaker open-source edition. Contact [ProcessMaker Sales](https://www.processmaker.com/contact/) or ask your ProcessMaker sales representative how the Data Connector connector can be installed in your ProcessMaker instance.

### Make a Copy of an Existing Data Connector Connector Instead of Adding One?

See [Copy Process Model Elements or Connectors](../../copy-process-model-elements-or-connectors.md).

### Permissions Required

Your ProcessMaker user account or group membership must have the following permissions to add a Data Connector connector to the Process model unless your user account has the **Make this user a Super Admin** setting selected:

* Processes: Edit Processes
* Processes: View Processes

See the [Process](../../../../processmaker-administration/permission-descriptions-for-users-and-groups.md#processes) permissions or ask your ProcessMaker Administrator for assistance.
{% endhint %}

Follow these steps to add a Data Connector connector to the Process model:

1. [View your Processes](../../../viewing-processes/view-the-list-of-processes/view-your-processes.md#view-all-active-processes). The **Processes** page displays.
2. [Create a new Process](../../../viewing-processes/view-the-list-of-processes/create-a-process.md) or click the **Open Modeler** icon![](../../../../.gitbook/assets/open-modeler-edit-icon-processes-page-processes.png)to edit the selected Process model. Process Modeler displays.
3. Locate the **Data Connector** connector in the **Elements and Connectors** palette that is to the left of the Process Modeler canvas. If the [**Hide Menus** button](../../navigate-around-your-process-model.md#maximize-the-process-modeler-canvas-view)![](../../../../.gitbook/assets/hide-menus-button-process-modeler-processes.png)is enabled, the **Elements and Connectors** palette displays the **Data Connector** connector's icon![](../../../../.gitbook/assets/data-connector-icon-process-modeler-package-processes.png). ![](../../../../.gitbook/assets/data-connector-control-process-modeler-package-processes.png) 
4. Drag the connector into the Process model canvas where you want to place it. If a Pool element is in your Process model, the Data Connector connector cannot be placed outside of the Pool element.

![Data Connector connector](../../../../.gitbook/assets/data-connector-control-placed-process-modeler-package-processes.png)

{% hint style="info" %}
After adding the Data Connector connector, consider adding either of the following Boundary-type Process model elements to design business solutions when your best-case scenarios don't happen:

* [Boundary Timer Event](../../model-your-process/add-and-configure-boundary-timer-event-elements.md#add-a-boundary-timer-event-element) element \([Don't know what that is?](../../model-your-process/process-modeling-element-descriptions.md#boundary-timer-event)\)
* [Boundary Error Event](../../model-your-process/add-and-configure-boundary-error-event-elements.md#add-a-boundary-error-event-element) element \([Don't know what that is?](../../model-your-process/process-modeling-element-descriptions.md#boundary-error-event)\)
* [Boundary Signal Event](../../model-your-process/add-and-configure-boundary-signal-event-elements.md) element \([Don't know what that is?](../../model-your-process/process-modeling-element-descriptions.md#boundary-signal-event)\)
{% endhint %}

After the Data Connector connector is placed into the Process model, you may move it by dragging it to the new location.

{% hint style="warning" %}
Moving a Data Connector connector has the following limitations in regards to the following Process model elements:

* **Pool element:** If the Data Connector connector is inside of a [Pool](../../model-your-process/process-modeling-element-descriptions.md#pool) element, it cannot be moved outside of the Pool element. If you attempt to do so, Process Modeler places the Data Connector connector inside the Pool element closest to where you attempt to move it.
* **Lane element:** If the Data Connector connector is inside of a Lane element, it can be moved to another Lane element in the same Pool element. However, the Data Connector connector cannot be moved outside of the Pool element.
{% endhint %}

## Settings

{% hint style="info" %}
### ProcessMaker Package Required

The [Data Connector package](../../../../package-development-distribution/package-a-connector/data-connector-package.md) is required. The Data Connector [package](../../../../package-development-distribution/first-topic.md) installs the Data Connector connector, which is not available in the ProcessMaker open-source edition. Contact [ProcessMaker Sales](https://www.processmaker.com/contact/) or ask your ProcessMaker sales representative how the Data Connector connector can be installed in your ProcessMaker instance.

### Permissions Required

Your ProcessMaker user account or group membership must have the following permissions to configure a Data Connector connector unless your user account has the **Make this user a Super Admin** setting selected:

* Processes: Edit Processes
* Processes: View Processes

See the [Process](../../../../processmaker-administration/permission-descriptions-for-users-and-groups.md#processes) permissions or ask your ProcessMaker Administrator for assistance.
{% endhint %}

The Data Connector connector has the following panels that contain settings:

* **Configuration** panel
  * [Edit the connector name](data-connector-connector.md#edit-the-control-name)
  * [Select the ProcessMaker Data Connector](data-connector-connector.md#select-the-processmaker-data-connector)
  * [Select the EndPoint to call from the ProcessMaker Data Connector](data-connector-connector.md#select-the-endpoint-to-call-from-the-processmaker-data-connector)
* **Data Mapping** panel
  * [Map data from the data source to the Request's JSON data Model](data-connector-connector.md#map-data-from-the-data-source-to-the-requests-json-data-model)

### Configuration Panel Settings

The Data Connector connector has the following settings in the **Configuration** panel:

* [Edit the connector name](data-connector-connector.md#edit-the-control-name)
* [Select the ProcessMaker Data Connector](data-connector-connector.md#select-the-processmaker-data-connector)
* [Select the EndPoint the Data Connector connector uses to interact with the data source](data-connector-connector.md#select-the-endpoint-the-data-connector-control-uses-to-interact-with-the-data-source)

#### Edit the Connector Name

A connector name is a human-readable reference for a Process model control. Process Modeler automatically assigns the name of a Process model connector with its connector type. However, a connector's name can be changed.

Follow these steps to edit the name for a Data Connector connector:

1. Ensure that the **Hide Menus** button![](../../../../.gitbook/assets/hide-menus-button-process-modeler-processes.png)is not enabled. See [Maximize the Process Modeler Canvas View](../../navigate-around-your-process-model.md#maximize-the-process-modeler-canvas-view).
2. Select the Data Connector connector from the Process model in which to edit its name. Panels to configure this connector display.
3. Expand the **Configuration** panel if it is not presently expanded. The **Name** setting displays. ![](../../../../.gitbook/assets/data-connector-configuration-name-process-modeler-processes.png) 
4. In the **Name** setting, edit the selected connector's name and then press **Enter**.

#### Select the ProcessMaker Data Connector

The Data Connector connector uses a [ProcessMaker Data Connector](../../../data-connector-management/what-is-a-data-connector.md) that is configured to interact with a data source, such as a [ProcessMaker Collection](../../../../collections/what-is-a-collection.md) or a third-party Application Program Interface \(API\). A ProcessMaker Data Connector must already exist before it can be selected for use in a Data Connector connector. Each ProcessMaker Data Connector is already configured with which data source it interacts.

ProcessMaker Collections automatically create a Data Connector when the Collection is created. ProcessMaker Data Connectors created from a Collection by default have the same name as the Collection that it references.

Follow these steps to select the ProcessMaker Data Connector the Data Connector connector uses:

1. Ensure that the **Hide Menus** button![](../../../../.gitbook/assets/hide-menus-button-process-modeler-processes.png)is not enabled. See [Maximize the Process Modeler Canvas View](../../navigate-around-your-process-model.md#maximize-the-process-modeler-canvas-view).
2. Select the Data Connector connector from the Process model in which to specify the ProcessMaker Data Connector to reference. Panels to configure this connector display.
3. Expand the **Configuration** panel if it is not presently expanded, and then locate the **Data Connector** setting. ![](../../../../.gitbook/assets/data-connector-configuration-data-connector-process-modeler-processes.png) 
4. From the **Data Connector** drop-down menu, select which ProcessMaker Data Connector the Data Connector connector uses.
5. [Select which Endpoint the ProcessMaker Data Connector uses to interact with the data source](data-connector-connector.md#select-the-endpoint-to-call-from-the-processmaker-data-connector).

{% hint style="info" %}
Ensure to [select which Endpoint to call from the selected ProcessMaker Data Connector](data-connector-connector.md#select-the-endpoint-to-call-from-the-processmaker-data-connector) to properly configure the Data Connector connector.
{% endhint %}

#### Select the EndPoint the Data Connector Connector Uses to Interact with the Data Source

Each [ProcessMaker Data Connector](../../../data-connector-management/what-is-a-data-connector.md) contains at least one [Endpoint](../../../data-connector-management/what-is-an-endpoint.md). These Endpoints are configured from the ProcessMaker Data Connector itself. An Endpoint is an action the ProcessMaker Data Connector uses to interact with the data source. The Data Connector connector uses an Endpoint to interact with the data source. These Endpoints may interact with [ProcessMaker Collection](../../../../collections/what-is-a-collection.md) records, Application Program Interfaces \(APIs\), or other data source types. After a ProcessMaker Data Connector has been selected from the [**Data Connector** setting](data-connector-connector.md#select-the-processmaker-data-connector), select the Endpoint from that ProcessMaker Data Connector the Data Connector uses to interact with the data source.

ProcessMaker Data Connectors created from Collections use a default set of Endpoints. See [Endpoints for ProcessMaker Collections](../../../data-connector-management/what-is-an-endpoint.md#endpoints-for-processmaker-collections).

Follow these steps to select which Endpoint the Data Connector connector uses:

1. Ensure that the **Hide Menus** button![](../../../../.gitbook/assets/hide-menus-button-process-modeler-processes.png)is not enabled. See [Maximize the Process Modeler Canvas View](../../navigate-around-your-process-model.md#maximize-the-process-modeler-canvas-view).
2. Select the Data Connector connector from the Process model in which to select the Endpoint the ProcessMaker Data Connector uses. Panels to configure this connector display.
3. Expand the **Configuration** panel if it is not presently expanded then locate the **Data Connector** setting. Ensure that a ProcessMaker Data Connector is selected from the **Data Connector** setting. If not, see [Select the ProcessMaker Data Connector](data-connector-connector.md#select-the-processmaker-data-connector).
4. Locate the **Endpoint** setting. ![](../../../../.gitbook/assets/data-connector-configuration-endpoint-process-modeler-processes.png) 
5. From the **Endpoint** drop-down menu, select which Endpoint the Data Connector connector uses to interact with the data source.

### Data Mapping Panel Settings

The Data Connector connector has the following setting in the **Data Mapping** panel:

* [Map data from the data source to the Request's JSON data Model](data-connector-connector.md#map-data-from-the-data-source-to-the-requests-json-data-model)

#### Map Data from the Data Source to the Request's JSON Data Model

After [configuring which ProcessMaker Data Connector and Endpoint the Data Connector connector uses](data-connector-connector.md#configuration-panel-settings) to interact with the data source, specify how data from that data source integrates with [Request](../../../../using-processmaker/requests/what-is-a-request.md) data. After data integrates from the data source into the JSON data model for each Request started from your Process, make business decisions based on that data and reference it from [ProcessMaker Screens](../../../design-forms/what-is-a-form.md), [ProcessMaker Scripts](../../../scripts/what-is-a-script.md), and [ProcessMaker Collections](../../../../collections/what-is-a-collection.md).

The procedure to integrate the data source's data to the Request JSON data model is called mapping: specify the JSON object\(s\) in the JSON data model to store the data source's data. Each JSON object contains a key name which references the JSON object, and the value for that key. If the JSON object already exists in a Request's JSON data model, then the Data Connector connector overwrites the existing JSON object value with that from the data source. If the JSON object\(s\) to map the data source data does not exist, then the Data Connector connector adds the JSON data object\(s\) to that Request's JSON data model.

Follow these steps to specify the Request JSON data object\(s\) to which to map the data source's data:

1. Ensure that the **Hide Menus** button![](../../../../.gitbook/assets/hide-menus-button-process-modeler-processes.png)is not enabled. See [Maximize the Process Modeler Canvas View](../../navigate-around-your-process-model.md#maximize-the-process-modeler-canvas-view).
2. Select the Data Connector connector from the Process model to map the data source's data to the Request JSON object\(s\). Panels to configure this connector display.
3. Expand the **Data Mapping** panel if it is not presently expanded. The **Form Data** setting displays. ![](../../../../.gitbook/assets/data-connector-form-data-mapping-package-processes.png) 
4. Click the **+Data** button to add a JSON object to which to map data from the data source. Settings display below the **key** and **value** columns to add the JSON key name and its value, respectively, for the JSON object. ![](../../../../.gitbook/assets/data-connector-form-data-mapping-key-value-package-processes.png) 
5. In the **key** setting, enter the key name for the JSON object.
6. In the **value** setting, enter the value for the JSON object.
7. Repeat Steps 4 through 6 for each JSON object required to store data from the data object.

{% hint style="info" %}
Click the **Delete** icon![](../../../../.gitbook/assets/delete-record-record-list-control-screens-builder-processes.png)to delete a JSON object from the **Form Data** setting.
{% endhint %}

## Related Topics

{% page-ref page="../../../../package-development-distribution/package-a-connector/data-connector-package.md" %}

{% page-ref page="../what-is-a-connector.md" %}

{% page-ref page="../../../data-connector-management/what-is-a-data-connector.md" %}

{% page-ref page="../../../../collections/what-is-a-collection.md" %}

{% page-ref page="../../../design-forms/what-is-a-form.md" %}

{% page-ref page="../../../scripts/what-is-a-script.md" %}

{% page-ref page="../../../../package-development-distribution/first-topic.md" %}

{% page-ref page="../../copy-process-model-elements-or-connectors.md" %}

{% page-ref page="../../remove-process-model-elements.md" %}
