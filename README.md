# Template Banking Notifications System API

Underlying all IT architectures are core systems of records that are often not readily available due to its complexity and connectivity concerns. System APIs provide a means of hiding that complexity from the user while exposing data and providing downstream insulation from any interface changes or rationalization of those systems. This API provides an implementation best practice for a notification service that integrates with multiple systems like Gmail and Twilio and exposes a RESTful interface that triggers a notification.

## Catalyst Accelerator for Banking & Retail

This API is one of many components included in [Catalyst Accelerator for Banking](/exchange/68ef9520-24e9-4cf2-b2f5-620025690913/catalyst-accelerator-for-banking/) and [Catalyst Accelerator for Retail](/exchange/68ef9520-24e9-4cf2-b2f5-620025690913/catalyst-accelerator-for-retail/). It provides organizations with connectivity assets that accelerate project delivery, including pre-built API designs and implementations that support core business processes. 

![534f3649-c2b8-407d-8208-eb91a19efe75-image.png](https://exchange2-file-upload-service-kprod.s3.us-east-1.amazonaws.com:443/534f3649-c2b8-407d-8208-eb91a19efe75-image.png)

### License Agreement

This template is subject to the conditions of the [MuleSoft License Agreement](https://s3.amazonaws.com/templates-examples/AnypointTemplateLicense.pdf). Review the terms of the license before downloading and using this template. You can use this template for free with the Mule Enterprise Edition, CloudHub, or as a trial in Anypoint Studio. 

# Use Case

This API allows to send notifications via email as well as text messages via Twilio based on the input JSON message.

# Considerations

To get this template to run, there are preconditions to consider. Failing to do so can lead to unexpected behavior of the template.

- **APIs security considerations** - Deploy this API on CloudHub and manage using Runtime Manager.

## Run Stand Alone
In this section we detail the way you should run your template on your computer.

### Where to Download Anypoint Studio and the Mule Runtime

If you are new to Mule, download this software:

- [Download Anypoint Studio](https://www.mulesoft.com/platform/studio)
- [Download Mule runtime](https://www.mulesoft.com/lp/dl/mule-esb-enterprise)

### Import Template in Studio

In Studio, click the Exchange X icon in the upper left of the taskbar, log in with your
Anypoint Platform credentials, search for the template, and click **Open**.

### Run in Studio

After opening your template in Anypoint Studio, follow these steps to run it:

1. Locate the properties file `mule.dev.properties`, in src/main/resources.
2. Complete all the properties in the "Properties to Configure" section.
3. Right click the template project folder.
4. Hover your mouse over `Run as`.
5. Click `Mule Application (configure)`.
6. Inside the dialog, select Environment and set the variable `mule.env` to the value `dev`.
7. Click `Run`.

### Run Stand Alone 

Complete all properties in one of the property files, for example in mule.prod.properties and run your app with the corresponding environment variable to use it. To follow the example, use `mule.env=prod`. 

## Run in CloudHub
After adding your application to Runtime Manager, go to Manage Application > Properties to set the environment variables listed in the "Properties to Configure" section.

### Deploy in CloudHub
In Studio, right click your project name in Package Explorer and select Anypoint Platform > Deploy on CloudHub.

## Properties to Configure
To use this template you need to configure properties (credentials, configurations, etc.) either in a properties file or in Runtime Manager as Environment Variables. 

### Application Properties

- http.port `8081`

### SMTP Services Configuration

- smtp.host `smtp.gmail.com`
- smtp.port `465`
- smtp.user `your_username`
- smtp.password `your_password`

### Twilio Services Configuration

- twilio.phone.number `+10000000000`
- twilio.account.sid `dnZAVKAsDDOVMK7pHxO7`
- twilio.account.auth.token `bJ5P1ELET7ibq2TAHTgB`
