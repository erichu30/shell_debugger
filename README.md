Use debugger.sh to debug shell script
- create a file descriptor 111
- set the Generic POSIX shell variables stored in `$SHELLOPTS`
	- BASH_XTRACEFD
		- the file descriptor that xstrace direct to (default: 2, stderr), we set it to 111 in the sub-shell
	- PS4
		- the value is printed before each command bash displays during an execution trace
- redirect all trace stdout to fd 111, which is assined to the log file
