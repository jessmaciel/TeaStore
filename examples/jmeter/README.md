# JMeter Files #

Description of each JMeter file

1. Default TeaStore browser profile to use without gui: [teastore_browse_nogui](/examples/jmeter/teastore_browse_nogui.jmx) 
2. Default TeaStore browser profile: [teastore_browse_nogui](/examples/jmeter/teastore_browse.jmx)
3. Browser profile with Constant Throughput Timer plugin to determine the maximum throughput per minute (base 6000.0): [teastore_browse_limited_tp](/examples/jmeter/teastore_browse_limited_tp.jmx)
4. Browser profile with Stepping Thread Group: [teastore_browse_stepping](/examples/jmeter/teastore_browse_stepping.jmx)
5. Profile to exploit RAM vulnerability: [teastore_attackram_login](/examples/jmeter/teastore_attackram_login.jmx)
6. Profile to exploit CPU vulnerability: [teastore_attackcpu_login](/examples/jmeter/teastore_attackcpu_login.jmx)
7. Only /loginAction requests: [teastore_dobem_login](/examples/jmeter/teastore_dobem_login.jmx)



## Changeable fields ##

### JMeter basics ###

Duration of the running. 
Replace _DURATION_IN_SECONDS_ (e.g., 2700)
```
<stringProp name="ThreadGroup.duration">DURATION_IN_SECONDS</stringProp>
```

### Constant Throughput Timer ###

Replace _TOTAL_THROUGHPUT_PER_MINUTE_ (eg. 6000.0)
```
<ConstantThroughputTimer guiclass="TestBeanGUI" testclass="ConstantThroughputTimer" testname="Constant>
          <intProp name="calcMode">2</intProp>
          <doubleProp>
            <name>throughput</name>
            <value>TOTAL_THROUGHPUT_PER_MINUTE</value>
            <savedValue>0.0</savedValue>
          </doubleProp>
        </ConstantThroughputTimer>

```
