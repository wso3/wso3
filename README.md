# WSO 3.0
The original version by oRb has become outdated from using functions that are now deprecated and was in need of an update so I have made many improvements and fixes to it.

If you have any feature requests or bugs to report feel free to submit via Issues
# Changelog October 2020
### SQL Manager
 - Changed SQL Form to not need base64 decode button
### Network
- Added netcat bind shell
- It now prints out backconnect command used
### Sec Info
- Added some more URLs to AWS tool
- Fixed phpinfo colors
### Console
- Added proc_open to command exec
### Other
- Changed highlight view for files to default
- Changed highlight colors
- Made eval on its own line with one variable (less obvious when in grep output)
- Decreased filesize

# Changelog March 2020
### SQL Manager
- Fixed bug in python backconnect where os.getenv('PATH') returns a None object
- Fixed SQL bugs, added error messages for connection failures
- Wrote support for PDO MySQL but removed as it causes shell to fail on older PHP installs
### Network
- Fixed default PATH for python reverse shells
- Fixed bug in python backconnect where os.getenv('PATH') returns a None object
- Made all system command backconnects run in background so next page loads
### Other
- Replaced all htmlspecialchars function calls with custom function to avoid [this bug](https://bugs.php.net/bug.php?id=47494)
- General code cleanup and bugfixes

# Changelog June 2018:
###  Removals
- String tools did not provide any useful functionality so I removed it
### Bugfixes
-   Fixed print file bug. On occasion the top of the file would fail to be displayed properly. This was due to htmlspecialchars being buggy. Fixed by implementing custom htmlspecialchars function
-   Added a base64 decode params button to deal with times when you go back on SQL Manager as now when forms are entered all parameters are base64 encoded to bypass basic WAFs
-   Fixed PostgreSQL. It wasn't implemented properly so I fixed it.
### SQL Manager
-   Added MySQLi support as MySQL is deprecated in PHP7
-   Added ODBC support (MSSQL and others use ODBC)
-   Added a button to download results of an SQL query directly
### Sec Info
-   Added get_loaded_extensions to SecInfo
-   Added Amazon API tool (useful on AWS servers)
### Console
-   Added support for Python, Perl and Lua command exec via the PHP extensions
-   Added COM exec code from fuhosin
###  Network
-   Added PHP, Ruby, Netcat and Socat backconnect options
-   Added Python TCP PTY and Python UDP PTY backconnect options that work with socat
-   Now the port box is automatically filled with a random port number and the Netcat and Socat commands to use are also given on the page
### Other Additions
-   Improved operation through WAFs (base64 all params)
-   Added Mass mailer
-   Noscript warning (to avoid confusion, you need to run JS for the shell to work)
-   Added Windows 1256 to charsets, may add more on request

