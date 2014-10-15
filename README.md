rtk-streamserver
================

Modified from str2str, a CUI AP of RTKLIB 2.4.2. The strsvrstat loop in the main function was modified by ddding some code to update the system time. Thus every time when the strsvrstat ( show stream server status ) executed, the GPS time in the GPS raw message will be extracted and be utilized to update the system time. If the difference between GPS time and system time is not big ( er than 1sec ), the system time will not update.

Usage example:
./str2str -in serial://ttyUSB0:115200:8:n:1:off#stq -out ntrips://:transient@192.168.10.110:2101/BASE1 -out serial://ttyS1:115200:8:n:1:off#rtcm3

The last -out option is used to make sure this program execute the strconv function, which contains the time extracting routine, since this function only executes when message format conversion is needed.
