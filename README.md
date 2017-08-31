# nagios_check_int_traffic

Script to check the interface bitrate in Mbps using SNMP

&nbsp;

## Usage

Usage: check_int_traffic HOSTADDR IF_NAME COMMUNITY DIRECTION MIN_VAL [[MID_MIN_VAL] [MID_MAX_VAL]] MAX_VAL

&nbsp;

HOSTADDR = Host IP address

IF_NAME = Interface name

COMMUNITY = SNMP Community

DIRECTION = Traffic direction - IN or OUT

MIN_VAL = Min value in Mbps: 1Gbps = 1000

MID_MIN_VAL = Min value to warning in Mbps: 3Gbps = 3000

MID_MAX_VAL = Max value to warning in Mbps: 8Gbps = 8000

MAX_VAL = Max value in Mbps: 10Gbps = 10000

&nbsp;

## Using with nagios

To use with nagios, copy the script to /usr/lib64/nagios/plugins/.

Edit the command file in /etc/nagios/conf.d:

```
define command{
        command_name    check_int_traffic
        command_line    $USER1$/check_int_traffic $ARG1$ $ARG2$ $ARG3$ $ARG4$ $ARG5$ $ARG6$ $ARG7$ $ARG8$
}
```
