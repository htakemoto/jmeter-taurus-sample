# Taurus Sample

Taurus improves experience of JMeter, Selenium and others.

https://gettaurus.org/


## Setup

install Taurus

```bash
brew install bzt
```

Apache JMeter will also be installed in `~/.bzt/jmeter-taurus/x.x.x/bin/jmeter`

## Quick Start


### Case1

```bash
bzt test-case1/quick_test.yml
```

### Case2

```bash
bzt test-case2/reservation-test.yml
```

Optional: you can also check on JMeter Console by executing the following command and click run button on JMeter Console.

```bash
bzt reservation-test.yml -gui
```

### Case3

```bash
bzt test-case3/test-with-jmeter.yml
```
