# Firewall Configuration and Testing

## Objective
To understand how firewall rules allow or block network traffic.

## Tool
iptables

## Commands Used

Display rules:

sudo iptables -L -n -v

Allow HTTP:

sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT

Block FTP:

sudo iptables -A INPUT -p tcp --dport 21 -j DROP

Verify rules:

sudo iptables -L -n -v

Remove FTP blocking rule:

sudo iptables -D INPUT -p tcp --dport 21 -j DROP

## Testing

1. Checked existing firewall rules.
2. Added an HTTP allow rule.
3. Added an FTP block rule.
4. Verified the updated rules.
5. Tested the effect in the authorized lab.
6. Removed the temporary FTP block rule.

## Observations

Record the actual results of your connectivity and scanning tests.

## Conclusion

Firewall rules provide control over incoming network traffic and help reduce unnecessary network exposure.
