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

## Finding the response time
<code> grep "time=" </code>
- grep: Global regular expression print is used for searching the content.

## Filtering the time and IP from previous Output
<code> awk '{print substr($7, 6, length($7)) " " substr($4, 1, length($4) -1)}' </code>
- awk(Aho, Weinberger, and Kernighan): Used to manipulate data. allows users to use variables and string functions and logical operators.
- {print substr($7, 6, length($7)) " " substr($4, 1, length($4) -1)} : print the substring of 7th column start=6 and end=total length and similarly the substring of 4th column is printed.

## Sort the output numerically
<code> sort -n </code>
- sort: Used to sort a file or arrange in some order.
- -n: Sort the file in numerical order.

## Print in the form {IP timems}
<code> awk '{print $2 " " $1 "ms"}' </code>
- awk: Allows users to use variables, string functions, and logical operators without compiling.
- {print $2 " " $1 "ms"}: print second column then first column, the delimiter is by default whitespace.

## Display the starting 10 lines
<code> head -n 10 </code>
- head: displays the starting 10 lines by default.
- -n 10: display the starting n lines. Here n is 10.

## Final Output
<code> curl -s http://public-dns.info/nameserver/br.csv | cut -d, -f1 | shuf | tail -n 50 | xargs -i timeout 1 ping -c1 -w 1 {} | grep "time=" | awk '{print substr($7, 6, length($7)) " " substr($4, 1, length($4) -1)}' | sort -n | awk '{print $2 " " $1 "ms"}' | head -n 10 </code>
<br>
**Output:**<br>
Displays 10 Hosts and the reponse time of each Host. The Host IP's are provided by the given URL.
<br>
