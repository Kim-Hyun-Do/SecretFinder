# SecretFinder

It is SecretFinder changed by r0b0ts.

# Upgrade Point

The origin code of SecretFinder can not read all js endpoints in a file not well. So, when a file containing a large amount of js endpoints is turned over to the input value, the results have not been successfully produced.(origin code: https://github.com/m4ll0k/SecretFinder)

Finally, I wanted SecretFinder can get all js endpoints and validate the js endpoints in a file successfully. Because I had the js endpoints from Burp-Suite and my web crawling methology.

# Help
```
usage: SecretFinder.py [-h] [-e] [-i INPUT] [-f FILE] [-o OUTPUT] [-r REGEX] [-b]
                       [-c COOKIE] [-g IGNORE] [-n ONLY] [-H HEADERS]
                       [-p PROXY]

optional arguments:
  -h, --help            show this help message and exit
  -e, --extract         Extract all javascript links located in a page and
                        process it
  -i INPUT, --input INPUT
                        Input a: URL, file or folder
  -f FILE, --file FILE
                        Input file with js endpoints
  -o OUTPUT, --output OUTPUT
                        Where to save the file, including file name. Default:
                        output.html
  -r REGEX, --regex REGEX
                        RegEx for filtering purposes against found endpoint
                        (e.g: ^/api/)
  -b, --burp            Support burp exported file
  -c COOKIE, --cookie COOKIE
                        Add cookies for authenticated JS files
  -g IGNORE, --ignore IGNORE
                        Ignore js url, if it contain the provided string
                        (string;string2..)
  -n ONLY, --only ONLY  Process js url, if it contain the provided string
                        (string;string2..)
  -H HEADERS, --headers HEADERS
                        Set headers ("Name:Value\nName:Value")
  -p PROXY, --proxy PROXY
                        Set proxy (host:port)

```

# Usage

`python3 SecretFinder.py -f ~/js_endpoints -o cli`

