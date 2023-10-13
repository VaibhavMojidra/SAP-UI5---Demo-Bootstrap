# SAP UI5 Demo Bootstrap


To run SAPUI5, we need to load and initialize it. This process of loading and initializing SAPUI5 is called bootstrapping. Once this bootstrapping is finished, we simply display an alert.

In this step, we load the SAPUI5 framework from our local webserver and initialize the core modules with the following configuration options:

The src attribute of the `<script>` tag tells the browser where to find the SAPUI5 core library – it initializes the SAPUI5 runtime and loads additional resources, such as the libraries specified in the data-sap-ui-libs attribute.

The SAPUI5 controls support different themes, we choose sap_belize as our default theme.

We specify the required UI library sap.m containing the UI controls we need for this tutorial.

To make use of the most recent functionality of SAPUI5 we define the compatibility version as edge.

We configure the process of “bootstrapping” to run asynchronously.

This means that the SAPUI5 resources can be loaded simultaneously in the background for performance reasons.

We define the module to be loaded initially in a declarative way. With this, we avoid directly executable JavaScript code in the HTML file. This makes your app more secure. We will create the script that this references to further down in this step.
We tell SAPUI5 core that resources in the sap.ui.demo.walkthrough namespace are located in the same folder as index.html. This is, for example, necessary for apps that run in the SAP Fiori launchpad.

> Method: `sap.ui.define`

The sap.ui.define function in SAP UI5 is used to define modules, such as creating new library classes1. This is typically the outermost frame of a module, its entry point so to say2. The dependencies that are listed in the sap.ui.define call will be resolved before the factory function (the function given as argument to the sap.ui.define call) will