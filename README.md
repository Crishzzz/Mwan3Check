# Mwan3Check
## Background
Under some specific public places, the bandwidth of wired access may be limited. For example, if the interface speed is 1000Mbps and the actual total available egress bandwidth of the system is 500Mbps, the actual bandwidth available to each user may only be about 30Mbps. To solve this problem, using port multi-dialling is a good choice.
## Motivation
mwan3 is a great multidialling program for load balancing and bandwidth stacking. However, because of program defects, equipment factors or human factors, a certain port of the mwan3 program may not work properly. In this case, it is necessary to design a programme that can automatically detect the status of the mwan3 programme and restart it when it is abnormal.
## Design ideas
In OpenWRT system, the command to view the status of mwan3 is `mwan3 status`, and you can see the output status after execution. With the help of this idea, `mwan3 status | grep offline` can be used to see if any port is offline. If the return value is null, then no ports are offline and the operation is normal, and vice versa. If an anomaly is detected, simply restarting the mwan3 service will usually solve the problem.
## Environment
**OS**:openwrt \
**Interpreter**: bash
## Contact
If you have any related questions or imporve ideas, please contact us: xuhaizzj@Gmail.com, very grateful !
