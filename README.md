# resourcechangetest

File -> New project, plus some custom build variants & source sets, to demonstrate changes to layout files not reaching the device after a build/deploy.

To reproduce I changed the text in this file

https://github.com/scb5304/resourcechangetest/blob/master/app/src/main/res/layout/fragment_first.xml

And redeployed and nothing changed.

Fixing the issue involves deleting the declaration of the custom resource source set.

https://github.com/scb5304/resourcechangetest/blob/master/app/build.gradle#L37

