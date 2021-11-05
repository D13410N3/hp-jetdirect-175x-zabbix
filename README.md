# hp-jetdirect-175x-zabbix
Zabbix pattern for print-server HP JetDirect 175x. Maybe it will work for any other print-servers, idk.

# Items (and some example)
- ethernet.admin.status
- ethernet.in.octets
- interface.ethernet.speed
- ethernet.mac
- ethernet.oper.status
- ethernet.out.octets
- icmppingloss (default ICMP zabbix)
- icmpping (default ICMP zabbix)
- icmppingsec (default ICMP zabbix)
- printer.job.status (0 or 1 if printer is printing now)
- printer.model.full (MFG:EPSON;CMD:ESCPL2,BDC,D4,D4PX;MDL:L210 Series;CLS:PRINTER;DES:EPSON L210 Series;CID:EpsonStd10;FID:FXN,DPN,WFN,ETN,AFN,DAN;RID:00;)
- printer.model.short (L210 Series)
- system.contact
- system.hostname
- system.location
- system.rom.version
- system.uptime
- system.mgmt.url

# Triggers
- No printer connected (printer.model.full.strlen() < 3)
- Default ICMP triggers (loss, time, unavailable)

# Graphs
- Printer Job
- Ethernet status (lol'd)
- Default ICMP Graphs
- Uptime

Written based on some mib-files in this repo.

Checked with Zabbix 5.4.0
