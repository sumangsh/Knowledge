# <font color="green">KQL Queries</font>

## <font color="blue">Performance Queries</font>

__Total Bytes Received by computer__

```kql
Perf
| where Computer contains @"uni1hpor"
| where (CounterName == "Bytes Total/sec" or CounterName == "Total Bytes Received")
| summarize BytesTotal = sum(CounterValue) by Computer
```

```kql
Perf
| where Computer contains @"uni1hpfs"
| where (CounterName == "Bytes Total/sec" or CounterName == "Total Bytes Received")
| where Computer == "uni1hpfs1"
```

```kql
Perf
| where Computer contains @"uni1hpfs"
| where (CounterName == "Bytes Total/sec" or CounterName == "Total Bytes Received")
| summarize BytesTotal = avg(CounterValue) by Computer
| sort by BytesTotal desc
```

__CPU Utilisation__
```kql
Perf 
|where Computer contains @"uni1hpap15" 
|where ObjectName == "Processor" and CounterName == "% Processor Time" and InstanceName == "_Total"
```

__Checking Disk Space__
```kql
Perf | where ObjectName == "LogicalDisk" and CounterName == "% Free Space" and Computer == "uni1hpsp1.olc1.openlinkcloud.com"  
| summarize AggregatedValue = avg(CounterValue) by InstanceName
```

__Checking Only C drive Space__
```kql
Perf | 
where ObjectName == "LogicalDisk" and CounterName == "% Free Space" and Computer == "uni1hpsp1.olc1.openlinkcloud.com" and InstanceName == "C:" 
| summarize AggregatedValue = avg(CounterValue) by InstanceName
```
__Check Diskspace on multiple computers__
```kql
Perf 
| where ObjectName == "LogicalDisk" and CounterName == "% Free Space" 
| where Computer contains "uni1hpsp1.olc1.openlinkcloud.com" or  Computer contains  "uni1hpsp2.olc1.openlinkcloud.com" or Computer contains  "uni1hpsp3.olc1.openlinkcloud.com" and InstanceName == "C:" 
| summarize AggregatedValue = avg(CounterValue) by Computer
```

```kql
Perf 
| where ObjectName == "LogicalDisk" and CounterName == "Free Megabytes" 
| where Computer contains "uni1hpsp1.olc1.openlinkcloud.com" and InstanceName == "C:" 
| summarize AggregatedValue = avg(CounterValue) by Computer
```

__Memory checks with 3 different counters__
```kql
Perf 
| where ObjectName == "Memory" and CounterName == "Available MBytes" 
| where Computer contains "uni1hpsp1.olc1.openlinkcloud.com"
| summarize AggregatedValue = avg(CounterValue) by Computer
```
```kql
Perf 
| where ObjectName == "Memory" and CounterName == "Committed Bytes" 
| where Computer contains "uni1hpsp1.olc1.openlinkcloud.com"
| summarize AggregatedValue = avg(CounterValue) by Computer
```
```kql
Perf 
| where ObjectName == "Memory" and CounterName == "% Committed Bytes In Use" 
| where Computer contains "uni1hpsp1.olc1.openlinkcloud.com"
| summarize AggregatedValue = avg(CounterValue) by Compute
```

__Memory Utilisation Report__
```kql
Perf 
| where ObjectName == "Memory" and CounterName == "% Committed Bytes In Use" 
| where Computer contains "uni2hpap33.olc1.openlinkcloud.com"
| summarize AggregatedValue = percentile(CounterValue, 90) by Computer, bin(TimeGenerated, 1h)
```
__CPU Utilization Report__
```kql
Perf 
|where Computer contains @"uni2hpap33" 
|where ObjectName == "Processor" and CounterName == "% Processor Time" and InstanceName == "_Total"
|summarize avg(CounterValue) by Computer, bin(TimeGenerated, 1h)
```
__Disk Read/Writes per second Report__
```kql
Perf
| where Computer contains @"uni2hpap33"
| where CounterName == "Disk Reads/sec"
| summarize avg(CounterValue) by Computer, bin(TimeGenerated, 1h)
| render timechart
```
```kql
Perf
| where Computer contains @"uni2hpap33"
| where CounterName == "Disk Writes/sec"
| summarize avg(CounterValue) by Computer, bin(TimeGenerated, 1h)
| render timechart
```
__Network Bytes Total/Sec__
```kql
Perf
| where Computer contains @"uni2hpap33"
| where ObjectName == "Network Interface" and CounterName == "Bytes Total/sec"
| summarize BytesTotal = avg(CounterValue) by Computer, bin(TimeGenerated, 1h)
| render timechart
```


## <font color="blue">Resource Graph Query</font>

__Check power status of filtered vms__
```kql
resources
| where type == "microsoft.compute/virtualmachines"
| where name hasprefix "ewe1npxa"
| project name, resourceGroup, State=properties['extended']['instanceView']['powerState']['code']
```
```kql
resources
| where type == "microsoft.compute/virtualmachines"
| extend statestring = properties['extended']['instanceView']['powerState']['code']
| project name, resourceGroup, State=split(statestring,"/")[-1]
```
__Power status of any particular vm__
```kql
resources
| where type == "microsoft.compute/virtualmachines"
| where name == "ewe1hosp2"
| project name, resourceGroup, State=properties['extended']['instanceView']['powerState']['code']
```

__List VM sizes__
```pwsh
$query = @"
resources
| where type == "microsoft.compute/virtualmachines"
| project name, resourceGroup, VMSize=properties['hardwareProfile']['vmSize']
"@
Search-AzGraph -Query $query
```

**With OS Disk Name**
```kql
resources
| where type == "microsoft.compute/virtualmachines"
| where name startswith "$vm_pattern"
| project name, resourceGroup, osDisk=properties['storageProfile']['osDisk']['name'],State=properties['extended']['instanceView']['powerState']['code']
```


