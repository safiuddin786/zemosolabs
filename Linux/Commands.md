# Commands Assignment

---

## Displaying the list of hots
<code> curl -s http://public-dns.info/nameserver/br.csv </code>
- curl: Used for transferring the data from or to server.
- -s: It enables the silent mode i.e. It doesn't show any progessbar or progress indicators.

## Displaying only IP Address
<code> cut -d, -f1 </code>
- cut: The cut command is used to select a specific column of a file
- -d,: used to define the delimiter. Here, delimiter is ','
- -f1: used to specify a column number

## Shuffle
<code>  shuf </code>
- shuf: gets the random permutions of the Input.

## Display last 50 IPs
<code> tail -n 50 </code>
- tail: Displays last 10 lines.
- -n: displays last n lines instead of 10.
- 50: last 50 lines.

## Ping Hosts
<code>  xargs -i timeout 1 ping -c 1 -w 1 {} </code>
- xargs: Used to convert input from standard input into arguments to a command.
- -i: allows us to get output into placeholder.
- timeout 1: terminate the command after 1 second
- ping: Used to check whether the host is reachable.
- -c 1: Stop after sending 1 packet.
- -w 1: Stop after 1 second.

## Finding the time
<code> grep "time=" </code>
- grep: Global regular expression print is used for searching the content.

## 