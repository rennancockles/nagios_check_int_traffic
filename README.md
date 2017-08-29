# nagios_check_int_traffic
Script to check the interface bitrate in Mbps using SNMP

To use with nagios, copy the script to /usr/lib64/nagios/plugins/.
Edit the command file in /etc/nagios/conf.d: 
```
  define command{
          command_name    check_int_traffic
          command_line    $USER1$/check_int_traffic $ARG1$ $ARG2$ $ARG3$ $ARG4$ $ARG5$ $ARG6$ $ARG7$ $ARG8$
  }
```
