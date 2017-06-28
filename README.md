# node-iptables-loadbalancer
A NodeJS Application Manager Using iptables nativ for loadbalancing High Performance


# Allow unpreviliged user to configure iptables
You can limit which commands user can run via __sudo__. Also, you could provide a _NOPASSWD_ option in _sudoers_ file in that user's context instead of using the encrypted password "feature".

Here is an example for allowing an unprivileged user to issue the restart of the __iptables__ service:

    geewid  ALL = (root) NOPASSWD: /sbin/service iptables restart, /sbin/service iptables reload

The commands list is comma-separated...

You could also use *Cmnd_Alias* feature:  

    Cmnd_Alias FOOBAR = /sbin/service iptables restart, /sbin/service iptables reload
    geewid  ALL = (root) NOPASSWD: FOOBAR
