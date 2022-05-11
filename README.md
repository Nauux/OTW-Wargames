# Level: Bandit

<br />
<br />
These are dirty notes. Later they will be better structured
<br />
The passwords of the connections have not been fully displayed. This is a support, it is not to solve your life... Good Luck

<br />
<br />
<br />
<br />
Welcome to OverTheWire!

If you find any problems, please report them to Steven or morla on
irc.overthewire.org.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ and /proc/ is disabled
  so that users can not snoop on eachother. Files and directories with
  easily guessable or short names will be periodically deleted!

  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few usefull tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /usr/local/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /usr/local/pwndbg/
    * peda (https://github.com/longld/peda.git) in /usr/local/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /usr/local/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)
    * checksec.sh (http://www.trapkit.de/tools/checksec.html) in /usr/local/bin/checksec.sh

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us through IRC on
  irc.overthewire.org #wargames.

  Enjoy your stay!




Level 0
==========

ssh bandit0@bandit.labs.overthewire.org -p 2220
<br />password: ban*****
<br />cd /home/bandit0
<br />cat readme
<br />	boJ9jbb*************



Level 1
==========

ssh bandit1@bandit.labs.overthewire.org -p 2220
<br />password: boJ9jbb************
<br />cd /home/bandit1
<br />ls -la
<br />cat ./-   // others alternatives: 
<br />              rev - | rev 
<br />              cat < -
<br />	CV1DtqXWVFXTv***********



Level 2
==========

ssh bandit2@bandit.labs.overthewire.org -p 2220
<br />password: CV1DtqXWVFXTvM2***********
<br />ls -la
<br />cat "spaces in this filename"  // others alternatives:  
<br />                                  cat + s + Tab
<br />	UmHadQclWmgdLO***********



Level 3
==========

ssh bandit3@bandit.labs.overthewire.org -p 2220
<br />password: UmHadQclWmgdL**********
<br />ls -la
<br />cd inhere
<br />ls -la
<br />cat .hidden
<br />	pIwrPrtPN36QI**********



Level 4
==========

ssh bandit4@bandit.labs.overthewire.org -p 2220
<br />password: pIwrPrtPN36Q**********
<br />file ./inhere/*
<br />cat ./inhere/-file07
<br />	koReBOKuID**********



Level 5
==========

ssh bandit5@bandit.labs.overthewire.org -p 2220
<br />password: koReBOKuIDD**********
<br />cd inhere
<br />ls -la maybehere*
<br />	maybehere07
<br />	-rw-r-----  1 root bandit5 1033 May  7  2020 .file2
<br />cat maybehere07/.file2
<br />	DXjZPULLxYr**********



Level 6
==========

ssh bandit6@bandit.labs.overthewire.org -p 2220
<br />password: DXjZPULLxYr17u**********
<br />find / -group bandit6 -user bandit7
<br />cat /var/lib/dpkg/info/bandit7.password
<br />	HKBPTKQnIay4Fw**********



Level 7
==========

ssh bandit7@bandit.labs.overthewire.org -p 2220
<br />password: HKBPTKQnIay4**********
<br />cat data.txt | grep "millionth"
<br />	cvX2JJa4CFALtq**********



Level 8
==========

ssh bandit8@bandit.labs.overthewire.org -p 2220
<br />password: cvX2JJa4CFAL**********
<br />sort data.txt | uniq -u
<br />	UsvVyFSfZZWbi**********



Level 9
==========

ssh bandit9@bandit.labs.overthewire.org -p 2220
<br />password: UsvVyFSfZZWbi6**********
<br />strings data.txt | grep "="
<br />	truKLdjsbJ5g7yy**********



Level 10
==========

ssh bandit10@bandit.labs.overthewire.org -p 2220
<br />password: truKLdjsbJ**********
<br />cat data.txt | base64 -d;
<br />	IFukwKGsFW8MO**********



Level 11
==========

ssh bandit11@bandit.labs.overthewire.org -p 2220
<br />password: IFukwKGsFW8**********
<br />cat data.txt
<br />	5Gr8L4qetPEsPk8**********
<br />Decode text (5Gr8L4qetPEsPk8***********) to text: 
<br />	5Te8Y4drgCRfCx8ug**********
<br />  Tool: https://rot13.com



Level 12
==========

ssh bandit12@bandit.labs.overthewire.org -p 2220
<br />password: 5Te8Y4drgCRfC**********
<br />mkdir /tmp/dump
<br />cat data.txt | xxd -r > /tmp/dump/hex2
<br />mv hex2 hex2.gz
<br />gzip -d hex2.gz
<br />mv hex2 hex2.bz
<br />bzip2 -d hex2.bz
<br />mv hex2 hex2.gz
<br />gzip -d hex2.gz
<br />mv hex2 hex2.tar
<br />tar -xf hex2.tar

<br />mv data5.bin data5.tar
<br />tar -xf data5.tar

<br />mv data6.bin data6.bz
<br />bzip2 -d data6.bz
<br />mv data6 data6.tar
<br />tar -xf data6.tar

<br />mv data8.bin data8.gz
<br />gzip -d data8.gz
<br />cat data8
<br />	The password is 8ZjyCRiBWFYk**********



Level 13
==========

ssh bandit13@bandit.labs.overthewire.org -p 2220
<br />password: 8ZjyCRiBWFYkneahH**********
<br />ssh bandit14@localhost -i sshkey.private
<br />cat /etc/bandit_pass/bandit14
<br />	4wcYUJFw0k0X**********



Level 14
==========

ssh bandit14@bandit.labs.overthewire.org -p 2220
<br />password: 4wcYUJFw0k0XLShl**********
<br />nc -vv localhost 30000
<br />	BfMYroe26WYalil7**********



Level 15
==========

<br />ssh bandit15@bandit.labs.overthewire.org -p 2220
<br />password: BfMYroe26WYal**********
<br />echo "BfMYroe26WYalil7*********" | openssl s_client -connect localhost:30001 -ign_eof
<br />cluFn7wTiGryun**********



Level 16
==========

ssh bandit16@bandit.labs.overthewire.org -p 2220
<br />password: cluFn7wTiGryu**********
	  
<br />nmap -p31000-32000 localhost

<br />Starting Nmap 7.40 ( https://nmap.org ) at 2022-01-16 13:32 CET
<br />Nmap scan report for localhost (127.0.0.1)
<br />Host is up (0.00035s latency).
<br />Not shown: 996 closed ports
<br />PORT      STATE SERVICE
<br />31046/tcp open  unknown
<br />31518/tcp open  unknown
<br />31691/tcp open  unknown
<br />31790/tcp open  unknown
<br />31960/tcp open  unknown


<br />echo "cluFn7wTiGryuny*********" | openssl s_client -connect localhost:31790 -ign_eof

<br />-----BEGIN RSA PRIVATE KEY-----
<br />MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
<br />imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
<br />Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
<br />DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
<br />JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
<br />x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
<br />KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
<br />J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
<br />d8WErY0gPxun8pbJ************************************************
<br />-----END RSA PRIVATE KEY-----


<br />mkdir /tmp/bandit17
<br />cd /tmp/bandit17
<br />vim 17.key
<br />chmod 400 17.key
<br />ssh -i 17.key bandit17@localhost
<br />cat /etc/bandit_pass/bandit17
<br />xLYVMN9WE5zQ5vH**********



Level 17
==========

ssh bandit17@bandit.labs.overthewire.org -p 2220
<br />password: xLYVMN9WE5zQ5**********

<br />diff passwords.new passwords.old
<br />42c42
<br />< kfBf3eYk5BPBR**********
<br />---
<br />> w0Yfolrc5bwjS4q**********



Level 18
==========

ssh bandit18@bandit.labs.overthewire.org -p 2220
<br />password: kfBf3eYk5BPBRzwj**********

<br />ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat /home/bandit18/readme"
<br />IueksS7Ubh8G3DCwVzrTd**********



Level 19
==========

ssh bandit19@bandit.labs.overthewire.org -p 2220
<br />password: IueksS7Ubh8G3DC**********
<br />./bandit20-do cat /etc/bandit_pass/bandit20
<br />	GbKksEFF4yrVs6il55v**********



Level 20
==========

ssh bandit20@bandit.labs.overthewire.org -p 2220
<br />fsword: GbKksEFF4yrVs6il5**********
<br />echo "GbKksEFF4yrVs6il*********" | nc -l localhost -p 1234 &
<br />./suconnect 1234
<br />	Read: GbKksEFF4yrVs6i**********
<br />	Password matches, sending next password
<br />	gE269g2h3mw3pw**********



Level 21
==========

ssh bandit21@bandit.labs.overthewire.org -p 2220
<br />password: gE269g2h3mw3pwg**********
<br />cd /etc/cron.d
<br />cat cronjob_bandit22
<br />	@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
<br />	* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

<br />cd /usr/bin
<br />cat cronjob_bandit22.sh
<br />	#!/bin/bash
<br />	chmod 644 /tmp/t7O6lds9S0Rq**********
<br />	cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQ**********

<br />cd /tmp
<br />cat t7O6lds9S0Rq**********
<br />	Yk7owGAcWjwMVRw**********



Level 22
==========

ssh bandit22@bandit.labs.overthewire.org -p 2220
<br />password: Yk7owGAcWjwMV**********
<br />cd /etc/cron.d
<br />cat cronjob_bandit23
<br />	@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
<br />	* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null

<br />cd /usr/bin
<br />cat cronjob_bandit23.sh

<br />	#!/bin/bash

<br />	myname=$(whoami)
<br />	mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

<br />	echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

<br />	cat /etc/bandit_pass/$myname > /tmp/$mytarget


<br />myname=bandit23
<br />echo I am user $myname | md5sum | cut -d ' ' -f 1
<br />cat /tmp/8ca319486bfbbc36**********
<br />	jc1udXuA1tiHqjI**********



Level 23
==========

<br />ssh bandit23@bandit.labs.overthewire.org -p 2220
<br />password: jc1udXuA1tiH**********

<br />
<br />
<br />There are still challenges to be solved... :)

