### Step 1: Run the (incomplete) starter code
1.In your shell, run:

```
$ cd ipv10_p4
$ ./run.sh
```

This will:
*compile ip4v_forward.p4, and
*start a Mininet instance with three switches 's1' configured in a triangle, each connected to one host 'h1', 'h2'.
*The hosts are assigned IPs of 10.0.1.10, 10.0.2.10, etc.

2.You should now see a Mininet command prompt. Open two terminals for 'h1' and 'h2', respectively:

```
mininet> xterm h1 h2
```

3.Each host includes a small Python-based messaging client and server. In h2's xterm, start the server:
```
$ ./receive.py
```

4.In 'h1''s xterm, send a message from the client:
```
$ ./send_ipv4_addr.py 10.0.2.10 "P4 is cool"
```

or

```
$ ./send_ipv6_addr.py fe80::5678 "P4 is cool"
```
The message will be received.

5.Type 'exit' to leave each xterm and the Mininet command line.
```
mininet>exit


$./cleanup.sh
```

