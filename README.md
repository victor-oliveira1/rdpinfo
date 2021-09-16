# rdpinfo
Retrieve the hostname and domain (CN) from RDP server

## Description:
This script can get the hostname and domain (CN) from RDP server using xfreerdp program.

## Dependencies:
- bash
- xfreerdp

## Installation:
Just copy to a directory and add to the PATH environment variable.
Example:
>$ mkdir ~/.local/bin  
$ cp rdpinfo ~/.local/bin  
$ export PATH=$PATH:~/.local/bin

## Usage:
>rdpinfo [-t threads] target  
Options:  
-t Number of simultaneous worker threads (Default: 50)  
Arguments:  
target IP address or DNS name (+1 separated by space)

## Examples:
Scan one server:  
>$ rdpinfo 192.168.50.10  
** Starting rdpinfo with 50 threads **  
192.168.50.10	WINBOX.secdomain.lan  
** 1 host(s) scanned in 1 second(s) **  

Scaning a file containing some servers (One per line):
>$ rdpinfo $(cat servers.txt)  
** Starting rdpinfo with 50 threads **  
192.168.50.10	WINBOX.secdomain.lan  
192.168.50.11	WINBOX2.secdomain.lan  
192.168.50.12	WINBOX3.secdomain.lan  
** 3 host(s) scanned in 1 second(s) **  

Scaning some servers on cli:
>$ rdpinfo 192.168.50.10 192.168.50.11 192.168.50.12  
** Starting rdpinfo with 50 threads **  
192.168.50.10	WINBOX.secdomain.lan  
192.168.50.11	WINBOX2.secdomain.lan  
192.168.50.12	WINBOX3.secdomain.lan  
** 3 host(s) scanned in 1 second(s) **  

## Contact:
Victor Oliveira <victor.oliveira@gmx.com>