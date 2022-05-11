# Level: Bandit

*These are dirty notes. Later they will be better structured
*The passwords of the connections have not been fully displayed. This is a support, it is not to solve your life... Good Luck

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


==========================================================================



Level 0
==========

ssh bandit0@bandit.labs.overthewire.org -p 2220
password: ban*****
cd /home/bandit0
cat readme
	boJ9jbb*************



Level 1
==========

ssh bandit1@bandit.labs.overthewire.org -p 2220
password: boJ9jbb************
cd /home/bandit1
ls -la
cat ./-   // others alternatives: 
              rev - | rev 
              cat < -
	CV1DtqXWVFXTv***********



Level 2
==========

ssh bandit2@bandit.labs.overthewire.org -p 2220
password: CV1DtqXWVFXTvM2***********
ls -la
cat "spaces in this filename"  // others alternatives:  
                                  cat + s + Tab
	UmHadQclWmgdLO***********



Level 3
==========

ssh bandit3@bandit.labs.overthewire.org -p 2220
password: UmHadQclWmgdL**********
ls -la
cd inhere
ls -la
cat .hidden
	pIwrPrtPN36QI**********



Level 4
==========
ssh bandit4@bandit.labs.overthewire.org -p 2220
password: pIwrPrtPN36Q**********
file ./inhere/*
cat ./inhere/-file07
	koReBOKuID**********



Level 5
==========

ssh bandit5@bandit.labs.overthewire.org -p 2220
password: koReBOKuIDD**********
cd inhere
ls -la maybehere*
	maybehere07
	-rw-r-----  1 root bandit5 1033 May  7  2020 .file2
cat maybehere07/.file2
	DXjZPULLxYr**********



Level 6
==========

ssh bandit6@bandit.labs.overthewire.org -p 2220
password: DXjZPULLxYr17u**********
find / -group bandit6 -user bandit7
cat /var/lib/dpkg/info/bandit7.password
	HKBPTKQnIay4Fw**********



Level 7
==========

ssh bandit7@bandit.labs.overthewire.org -p 2220
password: HKBPTKQnIay4**********
cat data.txt | grep "millionth"
	cvX2JJa4CFALtq**********



Level 8
==========

ssh bandit8@bandit.labs.overthewire.org -p 2220
password: cvX2JJa4CFAL**********
sort data.txt | uniq -u
	UsvVyFSfZZWbi**********



Level 9
==========

ssh bandit9@bandit.labs.overthewire.org -p 2220
password: UsvVyFSfZZWbi6**********
strings data.txt | grep "="
	truKLdjsbJ5g7yy**********



Level 10
==========

ssh bandit10@bandit.labs.overthewire.org -p 2220
password: truKLdjsbJ**********
cat data.txt | base64 -d;
	IFukwKGsFW8MO**********



Level 11
==========

ssh bandit11@bandit.labs.overthewire.org -p 2220
password: IFukwKGsFW8**********
cat data.txt
	5Gr8L4qetPEsPk8**********
Decode text (5Gr8L4qetPEsPk8***********) to text: 
	5Te8Y4drgCRfCx8ug**********
  Tool: https://rot13.com



Level 12
==========

ssh bandit12@bandit.labs.overthewire.org -p 2220
password: 5Te8Y4drgCRfC**********
mkdir /tmp/dump
cat data.txt | xxd -r > /tmp/dump/hex2
mv hex2 hex2.gz
gzip -d hex2.gz
mv hex2 hex2.bz
bzip2 -d hex2.bz
mv hex2 hex2.gz
gzip -d hex2.gz
mv hex2 hex2.tar
tar -xf hex2.tar

mv data5.bin data5.tar
tar -xf data5.tar

mv data6.bin data6.bz
bzip2 -d data6.bz
mv data6 data6.tar
tar -xf data6.tar

mv data8.bin data8.gz
gzip -d data8.gz
cat data8
	The password is 8ZjyCRiBWFYk**********



Level 13
==========

ssh bandit13@bandit.labs.overthewire.org -p 2220
password: 8ZjyCRiBWFYkneahH**********
ssh bandit14@localhost -i sshkey.private
cat /etc/bandit_pass/bandit14
	4wcYUJFw0k0X**********



Level 14
==========

ssh bandit14@bandit.labs.overthewire.org -p 2220
password: 4wcYUJFw0k0XLShl**********
nc -vv localhost 30000
	BfMYroe26WYalil7**********



Level 15
==========

ssh bandit15@bandit.labs.overthewire.org -p 2220
password: BfMYroe26WYal**********
echo "BfMYroe26WYalil7*********" | openssl s_client -connect localhost:30001 -ign_eof

cluFn7wTiGryun**********



Level 16
==========

ssh bandit16@bandit.labs.overthewire.org -p 2220
password: cluFn7wTiGryu**********
	  
nmap -p31000-32000 localhost

Starting Nmap 7.40 ( https://nmap.org ) at 2022-01-16 13:32 CET
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00035s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown


echo "cluFn7wTiGryuny*********" | openssl s_client -connect localhost:31790 -ign_eof

-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJ************************************************
-----END RSA PRIVATE KEY-----


mkdir /tmp/bandit17
cd /tmp/bandit17
vim 17.key
chmod 400 17.key
ssh -i 17.key bandit17@localhost
cat /etc/bandit_pass/bandit17
xLYVMN9WE5zQ5vH**********



Level 17
==========

ssh bandit17@bandit.labs.overthewire.org -p 2220
password: xLYVMN9WE5zQ5**********

diff passwords.new passwords.old
42c42
< kfBf3eYk5BPBR**********
---
> w0Yfolrc5bwjS4q**********



Level 18
==========

ssh bandit18@bandit.labs.overthewire.org -p 2220
password: kfBf3eYk5BPBRzwj**********

ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat /home/bandit18/readme"
IueksS7Ubh8G3DCwVzrTd**********



Level 19
==========

ssh bandit19@bandit.labs.overthewire.org -p 2220
password: IueksS7Ubh8G3DC**********
./bandit20-do cat /etc/bandit_pass/bandit20
	GbKksEFF4yrVs6il55v**********



Level 20
==========

ssh bandit20@bandit.labs.overthewire.org -p 2220
fsword: GbKksEFF4yrVs6il5**********
echo "GbKksEFF4yrVs6il*********" | nc -l localhost -p 1234 &
./suconnect 1234
	Read: GbKksEFF4yrVs6i**********
	Password matches, sending next password
	gE269g2h3mw3pw**********



Level 21
==========

ssh bandit21@bandit.labs.overthewire.org -p 2220
password: gE269g2h3mw3pwg**********
cd /etc/cron.d
cat cronjob_bandit22
	@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
	* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

cd /usr/bin
cat cronjob_bandit22.sh
	#!/bin/bash
	chmod 644 /tmp/t7O6lds9S0Rq**********
	cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQ**********

cd /tmp
cat t7O6lds9S0Rq**********
	Yk7owGAcWjwMVRw**********



Level 22
==========

ssh bandit22@bandit.labs.overthewire.org -p 2220
password: Yk7owGAcWjwMV**********
cd /etc/cron.d
cat cronjob_bandit23
	@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
	* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null

cd /usr/bin
cat cronjob_bandit23.sh

	#!/bin/bash

	myname=$(whoami)
	mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

	echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

	cat /etc/bandit_pass/$myname > /tmp/$mytarget


myname=bandit23
echo I am user $myname | md5sum | cut -d ' ' -f 1
cat /tmp/8ca319486bfbbc36**********
	jc1udXuA1tiHqjI**********



Level 23
==========

ssh bandit23@bandit.labs.overthewire.org -p 2220
password: jc1udXuA1tiH**********



There are still challenges to be solved... :)

