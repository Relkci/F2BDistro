# F2BDistro
@Krelkci Aug 2017
https://twitter.com/Krelkci
https://www.blackhillsinfosec.com/configure-distributed-fail2ban/


Fail2Ban Distro is a proof of concept that can be built and scaled.

Additional information can be found at Black Hills Information Security's Blog post:
 https://www.blackhillsinfosec.com/configure-distributed-fail2ban/

Files:

iptables-multiport.conf
Action file that includes information to write to the new “global” log file.
Replaces /etc/fail2ban/actions.d/iptables-multiport.conf

newbans.conf
Filter for the new “global” log file.
Move to /etc/fail2ban/filter.d/newbans.conf

Sshd.conf
Updated filter for SSHD, includes some additional SSH failures for key-based-auth.
Replaces /etc/fail2ban/filter.d/sshd.conf

Jail.local
Information to create the new global-log monitor instance.
Move to /etc/fail2ban/jail.local

fail2ban-with-distro.yml
Ansible Playbook to remotely deploy neccessary codes to add additional node.  You will need the key generated from the server.  Instructions to generate this key are on the blog post.


Fail2Ban: 
https://www.fail2ban.org/

SSHFS: 
https://github.com/libfuse/sshfs

Distributed Fail2Ban
https://www.blackhillsinfosec.com/configure-distributed-fail2ban/
