# ruteros_noip_update

script check your interface ip (if you use pppoe use pppoe interface or internet coming Ethernet port user port for interface)  and not same for stored (noip.txt) update to noip


setup
-----------------------------------------------------------
 
 1. pls copy noip.txt to ruter root
 2. copy /src/noip_clean.txt contetnt to new script (/systems script):
    $ modify your info in script:
        user " no-ip user name  "
        password " no-ip password"
        hosts [:toarray (" host1 "," test.com ")]
        inetinterface " pppoe-out / Ethernet1...10 "
        mailSend 2
        mailList [:toarray ("","")]

 3. setup Scheduler (On Evenet: /system script run your_script_name )
  