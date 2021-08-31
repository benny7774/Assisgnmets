# Reconnaissance in Nmap

	* The Deep Security Reconnaissance Scan feature allows the detection of network port scanning to the remote host. It can detect possible attack in your system.

	* To simulate different types of Reconnaissance Scan and check how Deep Security can detect it, you can use freeware cross-platform tool such as Nmap.

* nmap -v -A google.com by this command it shows OS version and TCP ports which are open

tarting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 09:35 IST
NSE: Loaded 153 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 09:35
Completed NSE at 09:35, 0.00s elapsed
Initiating NSE at 09:35
Completed NSE at 09:35, 0.00s elapsed
Initiating NSE at 09:35
Completed NSE at 09:35, 0.00s elapsed
Initiating Ping Scan at 09:35
Scanning google.com (216.58.200.142) [2 ports]
Completed Ping Scan at 09:35, 0.01s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 09:35
Completed Parallel DNS resolution of 1 host. at 09:35, 0.03s elapsed
Initiating Connect Scan at 09:35
Scanning google.com (216.58.200.142) [1000 ports]
Discovered open port 443/tcp on 216.58.200.142
Discovered open port 80/tcp on 216.58.200.142

* nmap -v -O (target IP) 192.168.0.1 enabling OS detection by the nmap

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 09:39 IST
Initiating Ping Scan at 09:39
Scanning google.com (142.250.205.238) [4 ports]
Completed Ping Scan at 09:39, 0.00s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 09:39
Completed Parallel DNS resolution of 1 host. at 09:39, 0.01s elapsed
Initiating SYN Stealth Scan at 09:39
Scanning google.com (142.250.205.238) [1000 ports]
Discovered open port 80/tcp on 142.250.205.238
Discovered open port 443/tcp on 142.250.205.238
Completed SYN Stealth Scan at 09:39, 4.23s elapsed (1000 total ports)
Initiating OS detection (try #1) against google.com (142.250.205.238)
Retrying OS detection (try #2) against google.com (142.250.205.238)
Nmap scan report for google.com (142.250.205.238)
Host is up (0.0035s latency).
Other addresses for google.com (not scanned): 2404:6800:4007:81b::200e
rDNS record for 142.250.205.238: maa05s28-in-f14.1e100.net
Not shown: 998 filtered ports
PORT    STATE SERVICE
80/tcp  open  http
443/tcp open  https
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Aggressive OS guesses: Brother MFC-7820N printer (94%), Digi Connect ME serial-to-Ethernet bridge (94%), Netgear SC101 Storage Central NAS device (91%), Aastra 480i IP Phone or Sun Remote System Control (RSC) (91%), Aastra 6731i VoIP phone or Apple AirPort Express WAP (91%), GoPro HERO3 camera (91%), Konica Minolta bizhub 250 printer (91%), OUYA game console (91%), Crestron MPC-M5 AV controller or Wago Kontakttechnik 750-852 PLC (86%)
No exact OS matches for host (test conditions non-ideal).

Read data files from: /usr/bin/../share/nmap
OS detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 9.98 seconds
           Raw packets sent: 2135 (98.924KB) | Rcvd: 12 (600B)

* nmap -v -sS (target IP) 192.168.0.1 scaning the network

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 09:44 IST
Initiating Ping Scan at 09:44
Scanning 192.168.0.1 [4 ports]
Completed Ping Scan at 09:44, 0.01s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 09:44
Completed Parallel DNS resolution of 1 host. at 09:44, 0.01s elapsed
Initiating SYN Stealth Scan at 09:44
Scanning 192.168.0.1 [1000 ports]
Discovered open port 80/tcp on 192.168.0.1
Discovered open port 22/tcp on 192.168.0.1
Discovered open port 443/tcp on 192.168.0.1
Discovered open port 53/tcp on 192.168.0.1
Discovered open port 1900/tcp on 192.168.0.1
Completed SYN Stealth Scan at 09:44, 0.26s elapsed (1000 total ports)
Nmap scan report for 192.168.0.1
Host is up (0.0069s latency).
Not shown: 995 closed ports
PORT     STATE SERVICE
22/tcp   open  ssh
53/tcp   open  domain
80/tcp   open  http
443/tcp  open  https
1900/tcp open  upnp

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.43 seconds
           Raw packets sent: 1004 (44.152KB) | Rcvd: 1001 (40.060KB)

* nmap -p 1-5000 192.168.0.1 is for scan the open ports in the networks

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 09:46 IST
Nmap scan report for 192.168.0.1
Host is up (0.012s latency).
Not shown: 4995 closed ports
PORT     STATE SERVICE
22/tcp   open  ssh
53/tcp   open  domain
80/tcp   open  http
443/tcp  open  https
1900/tcp open  upnp

Nmap done: 1 IP address (1 host up) scanned in 1.28 seconds

* nmap -v -sN (target IP) 192.168.0.1 is used for the scan TCP null scan

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 09:49 IST
Initiating Ping Scan at 09:49
Scanning 192.168.0.1 [4 ports]
Completed Ping Scan at 09:49, 0.01s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 09:49
Completed Parallel DNS resolution of 1 host. at 09:49, 0.01s elapsed
Initiating NULL Scan at 09:49
Scanning 192.168.0.1 [1000 ports]
Completed NULL Scan at 09:49, 4.02s elapsed (1000 total ports)
Nmap scan report for 192.168.0.1
Host is up (0.00031s latency).
All 1000 scanned ports on 192.168.0.1 are open|filtered

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 4.19 seconds
           Raw packets sent: 2007 (80.272KB) | Rcvd: 4 (160B)

* nmap -v --scanflags SYNFIN 192.168.0.1 is for scaning the SYN and FIN packets

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 09:55 IST
Initiating Ping Scan at 09:55
Scanning 192.168.0.1 [4 ports]
Completed Ping Scan at 09:55, 0.00s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 09:55
Completed Parallel DNS resolution of 1 host. at 09:55, 0.01s elapsed
Initiating SYN Stealth Scan at 09:55
Scanning 192.168.0.1 [1000 ports]
Discovered open port 443/tcp on 192.168.0.1
Discovered open port 22/tcp on 192.168.0.1
Discovered open port 80/tcp on 192.168.0.1
Discovered open port 53/tcp on 192.168.0.1
Discovered open port 1900/tcp on 192.168.0.1
Completed SYN Stealth Scan at 09:55, 0.25s elapsed (1000 total ports)
Nmap scan report for 192.168.0.1
Host is up (0.014s latency).
Not shown: 995 closed ports
PORT     STATE SERVICE
22/tcp   open  ssh
53/tcp   open  domain
80/tcp   open  http
443/tcp  open  https
1900/tcp open  upnp

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.34 seconds
           Raw packets sent: 1004 (44.152KB) | Rcvd: 1001 (40.060KB)


* nmap -v -sX 192.168.0.1 is for to scan the refuge packets with the URG, FIN and PSH

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 10:00 IST
Initiating Ping Scan at 10:00
Scanning 192.168.0.1 [4 ports]
Completed Ping Scan at 10:00, 0.00s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 10:00
Completed Parallel DNS resolution of 1 host. at 10:00, 0.01s elapsed
Initiating XMAS Scan at 10:00
Scanning 192.168.0.1 [1000 ports]
Completed XMAS Scan at 10:00, 4.02s elapsed (1000 total ports)
Nmap scan report for 192.168.0.1
Host is up (0.0014s latency).
All 1000 scanned ports on 192.168.0.1 are open|filtered

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 4.10 seconds
           Raw packets sent: 2007 (80.272KB) | Rcvd: 4 (160B)

* nmap -oG - -vv 192.168.0.0-255 is for to check find the ports up or down

# Nmap 7.91 scan initiated Mon Aug 30 14:52:11 2021 as: nmap -oG - -vv 192.168.0.0-255
# Ports scanned: TCP(1000;1,3-4,6-7,9,13,17,19-26,30,32-33,37,42-43,49,53,70,79-85,88-90,99-100,106,109-111,113,119,125,135,139,143-144,146,161,163,179,199,211-212,222,254-256,259,264,280,301,306,311,340,366,389,406-407,416-417,425,427,443-445,458,464-465,481,497,500,512-515,524,541,543-545,548,554-555,563,587,593,616-617,625,631,636,646,648,666-668,683,687,691,700,705,711,714,720,722,726,749,765,777,783,787,800-801,808,843,873,880,888,898,900-903,911-912,981,987,990,992-993,995,999-1002,1007,1009-1011,1021-1100,1102,1104-1108,1110-1114,1117,1119,1121-1124,1126,1130-1132,1137-1138,1141,1145,1147-1149,1151-1152,1154,1163-1166,1169,1174-1175,1183,1185-1187,1192,1198-1199,1201,1213,1216-1218,1233-1234,1236,1244,1247-1248,1259,1271-1272,1277,1287,1296,1300-1301,1309-1311,1322,1328,1334,1352,1417,1433-1434,1443,1455,1461,1494,1500-1501,1503,1521,1524,1533,1556,1580,1583,1594,1600,1641,1658,1666,1687-1688,1700,1717-1721,1723,1755,1761,1782-1783,1801,1805,1812,1839-1840,1862-1864,1875,1900,1914,1935,1947,1971-1972,1974,1984,1998-2010,2013,2020-2022,2030,2033-2035,2038,2040-2043,2045-2049,2065,2068,2099-2100,2103,2105-2107,2111,2119,2121,2126,2135,2144,2160-2161,2170,2179,2190-2191,2196,2200,2222,2251,2260,2288,2301,2323,2366,2381-2383,2393-2394,2399,2401,2492,2500,2522,2525,2557,2601-2602,2604-2605,2607-2608,2638,2701-2702,2710,2717-2718,2725,2800,2809,2811,2869,2875,2909-2910,2920,2967-2968,2998,3000-3001,3003,3005-3007,3011,3013,3017,3030-3031,3052,3071,3077,3128,3168,3211,3221,3260-3261,3268-3269,3283,3300-3301,3306,3322-3325,3333,3351,3367,3369-3372,3389-3390,3404,3476,3493,3517,3527,3546,3551,3580,3659,3689-3690,3703,3737,3766,3784,3800-3801,3809,3814,3826-3828,3851,3869,3871,3878,3880,3889,3905,3914,3918,3920,3945,3971,3986,3995,3998,4000-4006,4045,4111,4125-4126,4129,4224,4242,4279,4321,4343,4443-4446,4449,4550,4567,4662,4848,4899-4900,4998,5000-5004,5009,5030,5033,5050-5051,5054,5060-5061,5080,5087,5100-5102,5120,5190,5200,5214,5221-5222,5225-5226,5269,5280,5298,5357,5405,5414,5431-5432,5440,5500,5510,5544,5550,5555,5560,5566,5631,5633,5666,5678-5679,5718,5730,5800-5802,5810-5811,5815,5822,5825,5850,5859,5862,5877,5900-5904,5906-5907,5910-5911,5915,5922,5925,5950,5952,5959-5963,5987-5989,5998-6007,6009,6025,6059,6100-6101,6106,6112,6123,6129,6156,6346,6389,6502,6510,6543,6547,6565-6567,6580,6646,6666-6669,6689,6692,6699,6779,6788-6789,6792,6839,6881,6901,6969,7000-7002,7004,7007,7019,7025,7070,7100,7103,7106,7200-7201,7402,7435,7443,7496,7512,7625,7627,7676,7741,7777-7778,7800,7911,7920-7921,7937-7938,7999-8002,8007-8011,8021-8022,8031,8042,8045,8080-8090,8093,8099-8100,8180-8181,8192-8194,8200,8222,8254,8290-8292,8300,8333,8383,8400,8402,8443,8500,8600,8649,8651-8652,8654,8701,8800,8873,8888,8899,8994,9000-9003,9009-9011,9040,9050,9071,9080-9081,9090-9091,9099-9103,9110-9111,9200,9207,9220,9290,9415,9418,9485,9500,9502-9503,9535,9575,9593-9595,9618,9666,9876-9878,9898,9900,9917,9929,9943-9944,9968,9998-10004,10009-10010,10012,10024-10025,10082,10180,10215,10243,10566,10616-10617,10621,10626,10628-10629,10778,11110-11111,11967,12000,12174,12265,12345,13456,13722,13782-13783,14000,14238,14441-14442,15000,15002-15004,15660,15742,16000-16001,16012,16016,16018,16080,16113,16992-16993,17877,17988,18040,18101,18988,19101,19283,19315,19350,19780,19801,19842,20000,20005,20031,20221-20222,20828,21571,22939,23502,24444,24800,25734-25735,26214,27000,27352-27353,27355-27356,27715,28201,30000,30718,30951,31038,31337,32768-32785,33354,33899,34571-34573,35500,38292,40193,40911,41511,42510,44176,44442-44443,44501,45100,48080,49152-49161,49163,49165,49167,49175-49176,49400,49999-50003,50006,50300,50389,50500,50636,50800,51103,51493,52673,52822,52848,52869,54045,54328,55055-55056,55555,55600,56737-56738,57294,57797,58080,60020,60443,61532,61900,62078,63331,64623,64680,65000,65129,65389) UDP(0;) SCTP(0;) PROTOCOLS(0;)
Host: 192.168.0.0 ()	Status: Down
Host: 192.168.0.1 ()	Status: Down
Host: 192.168.0.2 ()	Status: Down
Host: 192.168.0.3 ()	Status: Down
Host: 192.168.0.4 ()	Status: Down
Host: 192.168.0.5 ()	Status: Down
Host: 192.168.0.6 ()	Status: Down
Host: 192.168.0.7 ()	Status: Down
Host: 192.168.0.8 ()	Status: Down
Host: 192.168.0.9 ()	Status: Down
Host: 192.168.0.10 ()	Status: Down
Host: 192.168.0.11 ()	Status: Down
Host: 192.168.0.12 ()	Status: Down
Host: 192.168.0.13 ()	Status: Down
Host: 192.168.0.14 ()	Status: Down
Host: 192.168.0.15 ()	Status: Down
Host: 192.168.0.16 ()	Status: Down
Host: 192.168.0.17 ()	Status: Down
Host: 192.168.0.18 ()	Status: Down
Host: 192.168.0.19 ()	Status: Down
Host: 192.168.0.20 ()	Status: Down
Host: 192.168.0.21 ()	Status: Down
Host: 192.168.0.22 ()	Status: Down
Host: 192.168.0.23 ()	Status: Down
Host: 192.168.0.24 ()	Status: Down
Host: 192.168.0.25 ()	Status: Down
Host: 192.168.0.26 ()	Status: Down
Host: 192.168.0.27 ()	Status: Down
Host: 192.168.0.28 ()	Status: Down
Host: 192.168.0.29 ()	Status: Down
Host: 192.168.0.30 ()	Status: Down
Host: 192.168.0.31 ()	Status: Down
Host: 192.168.0.32 ()	Status: Down
Host: 192.168.0.33 ()	Status: Down
Host: 192.168.0.34 ()	Status: Down
Host: 192.168.0.35 ()	Status: Down
Host: 192.168.0.36 ()	Status: Down
Host: 192.168.0.37 ()	Status: Down
Host: 192.168.0.38 ()	Status: Down
Host: 192.168.0.39 ()	Status: Down
Host: 192.168.0.40 ()	Status: Down
Host: 192.168.0.41 ()	Status: Down
Host: 192.168.0.42 ()	Status: Down
Host: 192.168.0.43 ()	Status: Down
Host: 192.168.0.44 ()	Status: Down
Host: 192.168.0.45 ()	Status: Down
Host: 192.168.0.46 ()	Status: Down
Host: 192.168.0.47 ()	Status: Down
Host: 192.168.0.48 ()	Status: Down
Host: 192.168.0.49 ()	Status: Down
Host: 192.168.0.50 ()	Status: Down
Host: 192.168.0.51 ()	Status: Down
Host: 192.168.0.52 ()	Status: Down
Host: 192.168.0.53 ()	Status: Down
Host: 192.168.0.54 ()	Status: Down
Host: 192.168.0.55 ()	Status: Down
Host: 192.168.0.56 ()	Status: Down
Host: 192.168.0.57 ()	Status: Down
Host: 192.168.0.58 ()	Status: Down
Host: 192.168.0.59 ()	Status: Down
Host: 192.168.0.60 ()	Status: Down
Host: 192.168.0.61 ()	Status: Down
Host: 192.168.0.62 ()	Status: Down
Host: 192.168.0.63 ()	Status: Down
Host: 192.168.0.64 ()	Status: Down
Host: 192.168.0.65 ()	Status: Down
Host: 192.168.0.66 ()	Status: Down
Host: 192.168.0.67 ()	Status: Down
Host: 192.168.0.68 ()	Status: Down
Host: 192.168.0.69 ()	Status: Down
Host: 192.168.0.70 ()	Status: Down
Host: 192.168.0.71 ()	Status: Down
Host: 192.168.0.72 ()	Status: Down
Host: 192.168.0.73 ()	Status: Down
Host: 192.168.0.74 ()	Status: Down
Host: 192.168.0.75 ()	Status: Down
Host: 192.168.0.76 ()	Status: Down
Host: 192.168.0.77 ()	Status: Down
Host: 192.168.0.78 ()	Status: Down
Host: 192.168.0.79 ()	Status: Down
Host: 192.168.0.80 ()	Status: Down
Host: 192.168.0.81 ()	Status: Down
Host: 192.168.0.82 ()	Status: Down
Host: 192.168.0.83 ()	Status: Down
Host: 192.168.0.84 ()	Status: Down
Host: 192.168.0.85 ()	Status: Down
Host: 192.168.0.86 ()	Status: Down
Host: 192.168.0.87 ()	Status: Down
Host: 192.168.0.88 ()	Status: Down
Host: 192.168.0.89 ()	Status: Down
Host: 192.168.0.90 ()	Status: Down
Host: 192.168.0.91 ()	Status: Down
Host: 192.168.0.92 ()	Status: Down
Host: 192.168.0.93 ()	Status: Down
Host: 192.168.0.94 ()	Status: Down
Host: 192.168.0.95 ()	Status: Down
Host: 192.168.0.96 ()	Status: Down
Host: 192.168.0.97 ()	Status: Down
Host: 192.168.0.98 ()	Status: Down
Host: 192.168.0.99 ()	Status: Down
Host: 192.168.0.100 ()	Status: Down
Host: 192.168.0.101 ()	Status: Down
Host: 192.168.0.102 ()	Status: Down
Host: 192.168.0.103 ()	Status: Down
Host: 192.168.0.104 ()	Status: Down
Host: 192.168.0.105 ()	Status: Down
Host: 192.168.0.106 ()	Status: Down
Host: 192.168.0.107 ()	Status: Down
Host: 192.168.0.108 ()	Status: Down
Host: 192.168.0.109 ()	Status: Down
Host: 192.168.0.110 ()	Status: Down
Host: 192.168.0.111 ()	Status: Down
Host: 192.168.0.112 ()	Status: Down
Host: 192.168.0.113 ()	Status: Down
Host: 192.168.0.114 ()	Status: Down
Host: 192.168.0.115 ()	Status: Down
Host: 192.168.0.116 ()	Status: Down
Host: 192.168.0.117 ()	Status: Down
Host: 192.168.0.118 ()	Status: Down
Host: 192.168.0.119 ()	Status: Down
Host: 192.168.0.120 ()	Status: Down
Host: 192.168.0.121 ()	Status: Down
Host: 192.168.0.122 ()	Status: Down
Host: 192.168.0.123 ()	Status: Down
Host: 192.168.0.124 ()	Status: Down
Host: 192.168.0.125 ()	Status: Down
Host: 192.168.0.126 ()	Status: Down
Host: 192.168.0.127 ()	Status: Down
Host: 192.168.0.128 ()	Status: Down
Host: 192.168.0.129 ()	Status: Down
Host: 192.168.0.130 ()	Status: Down
Host: 192.168.0.131 ()	Status: Down
Host: 192.168.0.132 ()	Status: Down
Host: 192.168.0.133 ()	Status: Down
Host: 192.168.0.134 ()	Status: Down
Host: 192.168.0.135 ()	Status: Down
Host: 192.168.0.136 ()	Status: Down
Host: 192.168.0.137 ()	Status: Down
Host: 192.168.0.138 ()	Status: Down
Host: 192.168.0.139 ()	Status: Down
Host: 192.168.0.140 ()	Status: Down
Host: 192.168.0.141 ()	Status: Down
Host: 192.168.0.142 ()	Status: Down
Host: 192.168.0.143 ()	Status: Down
Host: 192.168.0.144 ()	Status: Down
Host: 192.168.0.145 ()	Status: Down
Host: 192.168.0.146 ()	Status: Down
Host: 192.168.0.147 ()	Status: Down
Host: 192.168.0.148 ()	Status: Down
Host: 192.168.0.149 ()	Status: Down
Host: 192.168.0.150 ()	Status: Down
Host: 192.168.0.151 ()	Status: Down
Host: 192.168.0.152 ()	Status: Down
Host: 192.168.0.153 ()	Status: Down
Host: 192.168.0.154 ()	Status: Down
Host: 192.168.0.155 ()	Status: Down
Host: 192.168.0.156 ()	Status: Down
Host: 192.168.0.157 ()	Status: Down
Host: 192.168.0.158 ()	Status: Down
Host: 192.168.0.159 ()	Status: Down
Host: 192.168.0.160 ()	Status: Down
Host: 192.168.0.161 ()	Status: Down
Host: 192.168.0.162 ()	Status: Down
Host: 192.168.0.163 ()	Status: Down
Host: 192.168.0.164 ()	Status: Down
Host: 192.168.0.165 ()	Status: Down
Host: 192.168.0.166 ()	Status: Down
Host: 192.168.0.167 ()	Status: Down
Host: 192.168.0.168 ()	Status: Down
Host: 192.168.0.169 ()	Status: Down
Host: 192.168.0.170 ()	Status: Down
Host: 192.168.0.171 ()	Status: Down
Host: 192.168.0.172 ()	Status: Down
Host: 192.168.0.173 ()	Status: Down
Host: 192.168.0.174 ()	Status: Down
Host: 192.168.0.175 ()	Status: Down
Host: 192.168.0.176 ()	Status: Down
Host: 192.168.0.177 ()	Status: Down
Host: 192.168.0.178 ()	Status: Down
Host: 192.168.0.180 ()	Status: Down
Host: 192.168.0.181 ()	Status: Down
Host: 192.168.0.182 ()	Status: Down
Host: 192.168.0.183 ()	Status: Down
Host: 192.168.0.184 ()	Status: Down
Host: 192.168.0.185 ()	Status: Down
Host: 192.168.0.186 ()	Status: Down
Host: 192.168.0.187 ()	Status: Down
Host: 192.168.0.188 ()	Status: Down
Host: 192.168.0.189 ()	Status: Down
Host: 192.168.0.190 ()	Status: Down
Host: 192.168.0.191 ()	Status: Down
Host: 192.168.0.192 ()	Status: Down
Host: 192.168.0.193 ()	Status: Down
Host: 192.168.0.194 ()	Status: Down
Host: 192.168.0.195 ()	Status: Down
Host: 192.168.0.196 ()	Status: Down
Host: 192.168.0.197 ()	Status: Down
Host: 192.168.0.198 ()	Status: Down
Host: 192.168.0.199 ()	Status: Down
Host: 192.168.0.200 ()	Status: Down
Host: 192.168.0.201 ()	Status: Down
Host: 192.168.0.202 ()	Status: Down
Host: 192.168.0.203 ()	Status: Down
Host: 192.168.0.204 ()	Status: Down
Host: 192.168.0.205 ()	Status: Down
Host: 192.168.0.206 ()	Status: Down
Host: 192.168.0.207 ()	Status: Down
Host: 192.168.0.208 ()	Status: Down
Host: 192.168.0.209 ()	Status: Down
Host: 192.168.0.210 ()	Status: Down
Host: 192.168.0.211 ()	Status: Down
Host: 192.168.0.212 ()	Status: Down
Host: 192.168.0.213 ()	Status: Down
Host: 192.168.0.214 ()	Status: Down
Host: 192.168.0.215 ()	Status: Down
Host: 192.168.0.216 ()	Status: Down
Host: 192.168.0.217 ()	Status: Down
Host: 192.168.0.218 ()	Status: Down
Host: 192.168.0.219 ()	Status: Down
Host: 192.168.0.220 ()	Status: Down
Host: 192.168.0.221 ()	Status: Down
Host: 192.168.0.223 ()	Status: Down
Host: 192.168.0.224 ()	Status: Down
Host: 192.168.0.225 ()	Status: Down
Host: 192.168.0.226 ()	Status: Down
Host: 192.168.0.227 ()	Status: Down
Host: 192.168.0.228 ()	Status: Down
Host: 192.168.0.229 ()	Status: Down
Host: 192.168.0.230 ()	Status: Down
Host: 192.168.0.231 ()	Status: Down
Host: 192.168.0.232 ()	Status: Down
Host: 192.168.0.233 ()	Status: Down
Host: 192.168.0.234 ()	Status: Down
Host: 192.168.0.235 ()	Status: Down
Host: 192.168.0.236 ()	Status: Down
Host: 192.168.0.237 ()	Status: Down
Host: 192.168.0.238 ()	Status: Down
Host: 192.168.0.239 ()	Status: Down
Host: 192.168.0.240 ()	Status: Down
Host: 192.168.0.241 ()	Status: Down
Host: 192.168.0.242 ()	Status: Down
Host: 192.168.0.243 ()	Status: Down
Host: 192.168.0.244 ()	Status: Down
Host: 192.168.0.245 ()	Status: Down
Host: 192.168.0.246 ()	Status: Down
Host: 192.168.0.247 ()	Status: Down
Host: 192.168.0.248 ()	Status: Down
Host: 192.168.0.249 ()	Status: Down
Host: 192.168.0.250 ()	Status: Down
Host: 192.168.0.251 ()	Status: Down
Host: 192.168.0.252 ()	Status: Down
Host: 192.168.0.253 ()	Status: Down
Host: 192.168.0.254 ()	Status: Down

* nmap -v --traceroute google.com is for trace hop path to each host

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 10:18 IST
Initiating Ping Scan at 10:18
Scanning google.com (142.250.77.142) [4 ports]
Completed Ping Scan at 10:18, 0.00s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 10:18
Completed Parallel DNS resolution of 1 host. at 10:18, 0.01s elapsed
Initiating SYN Stealth Scan at 10:18
Scanning google.com (142.250.77.142) [1000 ports]
Discovered open port 443/tcp on 142.250.77.142
Discovered open port 80/tcp on 142.250.77.142
Completed SYN Stealth Scan at 10:18, 4.85s elapsed (1000 total ports)
Initiating Traceroute at 10:18
Completed Traceroute at 10:18, 0.02s elapsed
Initiating Parallel DNS resolution of 1 host. at 10:18
Completed Parallel DNS resolution of 1 host. at 10:18, 13.00s elapsed
Nmap scan report for google.com (142.250.77.142)
Host is up (0.0019s latency).
Other addresses for google.com (not scanned): 2404:6800:4007:82c::200e
rDNS record for 142.250.77.142: maa05s16-in-f14.1e100.net
Not shown: 998 filtered ports
PORT    STATE SERVICE
80/tcp  open  http
443/tcp open  https

TRACEROUTE (using port 80/tcp)
HOP RTT     ADDRESS
1   1.60 ms 172.16.145.2
2   1.48 ms maa05s16-in-f14.1e100.net (142.250.77.142)

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 18.00 seconds
           Raw packets sent: 2014 (88.544KB) | Rcvd: 15 (636B)

* nmap -v --system-dns google.com is for to OS DNS resolver

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 10:28 IST
Initiating Ping Scan at 10:28
Scanning google.com (142.250.195.142) [4 ports]
Completed Ping Scan at 10:28, 0.00s elapsed (1 total hosts)
Initiating System DNS resolution of 1 host. at 10:28
Completed System DNS resolution of 1 host. at 10:28, 0.01s elapsed
Initiating SYN Stealth Scan at 10:28
Scanning google.com (142.250.195.142) [1000 ports]
Discovered open port 443/tcp on 142.250.195.142
Discovered open port 80/tcp on 142.250.195.142
Completed SYN Stealth Scan at 10:28, 4.53s elapsed (1000 total ports)
Nmap scan report for google.com (142.250.195.142)
Host is up (0.0068s latency).
Other addresses for google.com (not scanned): 2404:6800:4007:81f::200e
rDNS record for 142.250.195.142: maa03s40-in-f14.1e100.net
Not shown: 998 filtered ports
PORT    STATE SERVICE
80/tcp  open  http
443/tcp open  https

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 4.72 seconds
           Raw packets sent: 2004 (88.144KB) | Rcvd: 6 (252B)

* nmap -v -Pn google.com is for treat all host as online

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 10:34 IST
Initiating Parallel DNS resolution of 1 host. at 10:34
Completed Parallel DNS resolution of 1 host. at 10:34, 0.01s elapsed
Initiating Connect Scan at 10:34
Scanning google.com (142.250.77.110) [1000 ports]
Discovered open port 443/tcp on 142.250.77.110
Discovered open port 80/tcp on 142.250.77.110
Increasing send delay for 142.250.77.110 from 0 to 5 due to 11 out of 14 dropped probes since last increase.
Increasing send delay for 142.250.77.110 from 5 to 10 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for 142.250.77.110 from 10 to 20 due to 11 out of 11 dropped probes since last increase.
Increasing send delay for 142.250.77.110 from 20 to 40 due to 11 out of 11 dropped probes since last increase.
Completed Connect Scan at 10:35, 71.81s elapsed (1000 total ports)
Nmap scan report for google.com (142.250.77.110)
Host is up (0.0098s latency).
Other addresses for google.com (not scanned): 2404:6800:4007:81f::200e
rDNS record for 142.250.77.110: maa05s15-in-f14.1e100.net
Not shown: 998 filtered ports
PORT    STATE SERVICE
80/tcp  open  http
443/tcp open  https

Read data files from: /usr/bin/../share/nmap
Nmap done: 1 IP address (1 host up) scanned in 72.00 seconds

* nmap -v --dns-servers google.com is for specify custom dns

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 10:39 IST
Read data files from: /usr/bin/../share/nmap
Nmap done: 0 IP addresses (0 hosts up) scanned in 0.08 seconds
           Raw packets sent: 0 (0B) | Rcvd: 0 (0B)

* nmap -F google.com 192.168.0.1 is for fast scan of dns or ip

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 10:48 IST
Nmap scan report for google.com (142.250.182.14)
Host is up (0.012s latency).
Other addresses for google.com (not scanned): 2404:6800:4007:81b::200e
rDNS record for 142.250.182.14: maa05s18-in-f14.1e100.net
Not shown: 98 filtered ports
PORT    STATE SERVICE
80/tcp  open  http
443/tcp open  https

Nmap scan report for 192.168.0.1
Host is up (0.0071s latency).
Not shown: 95 closed ports
PORT     STATE SERVICE
22/tcp   open  ssh
53/tcp   open  domain
80/tcp   open  http
443/tcp  open  https
1900/tcp open  upnp

Nmap done: 2 IP addresses (2 hosts up) scanned in 2.00 seconds

* nmap -v -iR 10 -Ph -p is for iR is random port selection and Ph is treat all port as online and p is selected port

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 12:08 IST
Initiating Parallel DNS resolution of 10 hosts. at 12:08
Completed Parallel DNS resolution of 10 hosts. at 12:08, 13.00s elapsed
Initiating Connect Scan at 12:08
Scanning 10 hosts [1 port/host]
Discovered open port 80/tcp on 168.206.218.34
Completed Connect Scan at 12:08, 0.76s elapsed (10 total ports)
Nmap scan report for 202.248.129.1
Host is up (0.13s latency).

PORT   STATE  SERVICE
80/tcp closed http

Nmap scan report for 175.197.161.92
Host is up.

PORT   STATE    SERVICE
80/tcp filtered http

Nmap scan report for 35.120.136.201
Host is up.

PORT   STATE    SERVICE
80/tcp filtered http

Nmap scan report for p3171-ipngn5401hodogaya.kanagawa.ocn.ne.jp (180.13.66.171)
Host is up.

PORT   STATE    SERVICE
80/tcp filtered http

Nmap scan report for 168.206.218.34
Host is up (0.079s latency).

PORT   STATE SERVICE
80/tcp open  http

Nmap scan report for 101.22.148.77
Host is up.

PORT   STATE    SERVICE
80/tcp filtered http

Nmap scan report for 156.126.119.208
Host is up.

PORT   STATE    SERVICE
80/tcp filtered http

Nmap scan report for cpe-174-104-102-142.neo.res.rr.com (174.104.102.142)
Host is up.

PORT   STATE    SERVICE
80/tcp filtered http

Nmap scan report for 173.105.190.1
Host is up.

PORT   STATE    SERVICE
80/tcp filtered http

Nmap scan report for 40.red-83-40-49.dynamicip.rima-tde.net (83.40.49.40)
Host is up.

PORT   STATE    SERVICE
80/tcp filtered http

Read data files from: /usr/bin/../share/nmap
Nmap done: 10 IP addresses (10 hosts up) scanned in 13.87 seconds 

* nmap -PR 192.168.0.1/24 

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 12:12 IST
Nmap scan report for 192.168.0.1
Host is up (0.0074s latency).
Not shown: 995 closed ports
PORT     STATE SERVICE
22/tcp   open  ssh
53/tcp   open  domain
80/tcp   open  http
443/tcp  open  https
1900/tcp open  upnp

Nmap done: 256 IP addresses (1 host up) scanned in 4.42 seconds

* nmap -v --iflist google.com is for print host interfaces and routes

Starting Nmap 7.91 ( https://nmap.org ) at 2021-08-31 12:20 IST
************************INTERFACES************************
DEV  (SHORT) IP/MASK                     TYPE     UP MTU   MAC
lo   (lo)    127.0.0.1/8                 loopback up 65536
lo   (lo)    ::1/128                     loopback up 65536
eth0 (eth0)  172.16.145.130/24           ethernet up 1500  00:0C:29:40:87:DF
eth0 (eth0)  fe80::20c:29ff:fe40:87df/64 ethernet up 1500  00:0C:29:40:87:DF

**************************ROUTES**************************
DST/MASK                     DEV  METRIC GATEWAY
172.16.145.0/24              eth0 100
0.0.0.0/0                    eth0 100    172.16.145.2
::1/128                      lo   0
fe80::20c:29ff:fe40:87df/128 eth0 0
::1/128                      lo   256
fe80::/64                    eth0 100
ff00::/8                     eth0 256



