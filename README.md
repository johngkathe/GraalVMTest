# GraalVMTest

To all who want to look into playing around with this code, which in reality is a glorified "Hello World!" program using Java wrapped in JavaScript, you will need to have an up-to-date version of GraalVM, available here: https://github.com/graalvm/graalvm-ce-dev-builds/releases/tag/22.1.0-dev-20220127_2024


To get Node.js functionality for JavaScript, the following steps must be taken, as shown in Oracle's documentation: https://github.com/oracle/graaljs/tree/master/docs/user


I used the cross-env package from npm (https://www.npmjs.com/package/cross-env) to enable cross OS command line functionality for my script to call the NODE_PATH in package.json, which replaces the native Node path with the GraalVM Node path as follows:


(Naturally, you would change the path to fit your file path)
```
 "scripts": {
    "graal": "cross-env NODE_PATH=D:/GraalVM/graalvm-ce-java17-22.1.0-dev/bin/node.cmd node --polyglot --jvm index.js"
  }
```


This method required only the installation of node.cmd prior to running the script.


I think this is all you need to get this to run.  Enjoy!
