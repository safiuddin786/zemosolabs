# LINUX BASICS

---

## CURL
- **Transfer file from server** <br>
curl -O filename "url"
- **ftp server with username and password** <br>
curl -u username:password -O "url"
<br> *Note: -T for transfering file to server*

- **proxy in curl** (-x or -proxy both works) <br>
curl -x proxyname:port url
- **curl smtp** <br>
curl -url smtpurl -mail-from sendermail -mail-rcpt receivermail -n -ssl--reqd -u email:password -T mailtextfile

## Grep
*generally used with the pipe <br>
global regular expression print <br>*
<code> cat filename.txt | grep string </code>

## Cut
*select the specific column as the delimiter*<br>
cut -d- -f2