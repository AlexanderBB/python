# Simple network scanner 
Write on python build and test on 2.7.14

This is a simple network scanner, that supports multiple networks with CIDR and multipl ports.

# Install

Download the script and add execute permission. 
```
chmod +x net-scan
```
# Usage 

```
./net-scan -n 192.168.0.0/24 -p 80 --out-file /path/to/the/report.csv
```

This will scan all hosts in 192.168.0.0/24 network for port 80 and delivire the result on the console and in the file.

# Help

```
./net-scan -h 
```
Will show all possible options of the script

````
usage: net-scan [-h] -n ADDR/CIDR [ADDR/CIDR ...] -p PORT [PORT ...]
                [-of FILE] [-xml]

Scans network hosts for specific port.

optional arguments:
  -h, --help            show this help message and exit
  -of FILE, --out-file FILE
                        Output file location, with the scan results in CSV
                        format e.g. /path/to/some/dir/scan-results.csv
                        WARNING: Existing files will be overwritten!
  -xml                  Changes the out put format of the results to XML.

required arguments:
  -n ADDR/CIDR [ADDR/CIDR ...], --network ADDR/CIDR [ADDR/CIDR ...]
                        Network forward slash CIDR e.g. 191.168.0.0/16
                        Multiple networks suported, devided by space.
  -p PORT [PORT ...], --port PORT [PORT ...]
                        Enter port number for scanning. Value between 0-65535
                        e.g. 80 Multiple ports supported, devided by space.
````
