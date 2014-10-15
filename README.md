rtk-streamserver
================

Modified from str2str, a CUI AP of RTKLIB 2.4.2. The strsvrstat loop in the main function was modified by ddding some code to update the system time. Thus every time when the strsvrstat ( show stream server status ) executed, the GPS time in the GPS raw message will be extracted and be utilized to update the system time. If the difference between GPS time and system time is not big ( er than 1sec ), the system time will not update.
