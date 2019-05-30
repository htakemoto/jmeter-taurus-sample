# JMeter & Taurus Sample

This project contains 2 approaches, JMeter and Taurus+JMeter. You can skip JMeter Setup and jump to Taurus Setup.


## JMeter Setup

This project is based on JMeter version: 5.1.1

Reference: https://www.blazemeter.com/jmeter-tutorial (free for sign up to take courses)

### Install JMeter

```bash
brew install jmeter
```

### Install JMeter Plugins Manager

Go to https://jmeter-plugins.org/wiki/PluginsManager/ to download `jmeter-plugins-manager-x.x.jar` and copy to the following location:

```
/usr/local/Cellar/jmeter/5.1.1/libexec/lib/ext
```

### Start JMeter

```bash
jmeter
```

Note: JMeter has a new look! JMeter now has a Black GUI (the Darcula LAF theme). If you don't like it, you can always switch back through the 'Options->Look and Feel' menu.

Open `sample1.jmx` from JMeter GUI

Simple Test Script Structure
```
Test Plan
+- Thread Group
   +- User Defined Variables
   +- User Parameters
   +- HTTP Request
      +- Constant Timer
      +- Response Assertion
   +- View Results Tree
```


## Taurus Setup

Taurus improves experience of JMeter, Selenium and others.

https://gettaurus.org/

install Taurus

```bash
brew install bzt
```

Apache JMeter will also be installed in `~/.bzt/jmeter-taurus/x.x.x/bin/jmeter`

### Quick Start

#### Case1

```bash
bzt taurus/test-case1/quick_test.yml
```

#### Case2

```bash
bzt taurus/test-case2/reservation-test.yml
```

Optional: you can also check on JMeter Console by executing the following command and click run button on JMeter Console.

```bash
bzt taurus/test-case2/reservation-test.yml -gui
```

#### Case3

```bash
bzt taurus/test-case3/test-with-jmeter.yml
```
