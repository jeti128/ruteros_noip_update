# ruteros_noip_update

script check your interface ip (if you use pppoe use pppoe interface or internet coming Ethernet port user port for interface)  and not same for stored (noip.txt) update to noip
You like script send mail from update.

## setup

if you like send mail req mail setup in ruter (help) :

    https://wiki.mikrotik.com/wiki/Manual:Tools/email

    /tool e-mail> set server=10.1.1.1 port=25 from="router@mydomain.com"
    /tool e-mail
    set address=173.194.77.108
    set port=587
    set from=myuser@gmail.com
    set user=myuser
    set password=mypassword

copy /src/noip_clean.txt contetnt to new script (/systems script):

    modify your info in script
    user " no-ip user name  "
    password " no-ip password"
    hosts [:toarray (" host1 "," test.com ")]
    inetinterface " pppoe-out / Ethernet1...10 "
    mailSend 2 = not / 1 = send
    mailList [:toarray ("","")]

setup new Scheduler:

    On Evenet: /system script run your_script_name