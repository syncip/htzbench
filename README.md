# About htzbench
We try to perform a [yabs benchmark](https://github.com/masonr/yet-another-bench-script) on all hetzner servers and to collect and update the results.  
To get a certain statistical relevance, we try to make several benchmarks of each server (if possible there are 3 bechmarks on different days and times). Since this is very time-consuming and costly due to the number of servers that Hetzner offers, we are dependent on the help of the community. If you can support us with a benchmark result, please send it to us as a pull request.

# Result Overview
Date|Status|Type|Architecture|Size|Location|OS Image|yabs Version|Geekbench Link|Result Link
---|---|---|---|---|---|---|---|---|---
27.01.2024|fresh install|shared|x86|CX11|Nürnberg|Ubuntu 22.04|v2024-01-01|[Result](https://browser.geekbench.com/v6/cpu/4614102)|[Result](result/20240127_0_cx11_nuernberg.txt)|

## About the result file
How to read the name of the result file?  
Example: 20240127_0_cx11_nuernberg.txt

- year (2024), month (01) and day (17) of the benchmark  
- Bechmark Number (0)  
- Server Type (cx11) 
- Server Location (nürnberg)  

## What data do we collect collected?
- date
- status (fresh install, production server)
- type (shared or decdicated)
- architecture (x86 or arm)
- size (hetzner product name e.g. cx11)
- location
- image (ubuntu 22.04, debian bookworm, ...)
- yabs version
- geekbench link
- resulte link (raw yabs result output)

# Commit a result
If you have a result file, you can send it to this repository as a pull request. Please pay attention to the form of the result file and the naming (use an [example result](result/) for this).  
When submitting, please make sure that your server is not overloaded with other tasks (ideally the server is new). Do an update before a benchmark and make sure that your server is up to date.
We use the following procedure for our benchmarks:  
````
apt update & apt upgrade \
reboot
````

Make sure there are no more updates and run the benchmark.
````
apt update & apt upgrade \
curl -sL yabs.sh | bash
````