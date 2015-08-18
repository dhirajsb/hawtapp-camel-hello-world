# Camel CDI Hello world QuickStart

This quickstart shows a simple Apache Camel application that logs a message to the server log every 5th second.

This example is implemented using Camel CDI. The Camel routes are setup in the classe `MyRoutes` using an injected bean of class `SomeBean`, which counts the number of times it is invoked.

This example uses a timer to trigger every 5th second, and then writes a message to the server log.

The goal hawt-app:build MUST be called to create the hawt-app assembly as shown in the command below -

    mvn clean install hawt-app:build

# Running on OpenShift v3

If you would like to create an application template to start apps like this one on OpenShift v3, then just run the following OpenShift command:

   curl -s -L https://raw.githubusercontent.com/dhirajsb/hawtapp-camel-hello-world/master/os3-app-template.json | oc create -f -
   
This will add the 'fuse-hawt-app' App to the list of Apps that you can create in the OpenShift v3 console when you click the Add to project button.