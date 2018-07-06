# Surveys
 
These surveys are a work in progress collection of host enumeration scripts for Windows and NIX systems.
These scripts utilize system native scripting languages to determine OS/Distro/Kernel version and then execute a series of commands retreiving 3 different quantities (Brief / Standard / Verbose) of host information based on parameters passed in by the user.

------------------------------------------------------------------------------------------------------------------------------

## NIXserv

### USAGE:
  	NIXserv.sh -b/s/v -d 'YYYY-MM-DD HH:MM:SS' -o /<path>/<name>.txt 

### DESCRIPTION:
	NIXserv is a command line utility written to automate host survey and enumeration.
	The script begins by determining the distro and startup type of the system it is run on.
	It then proceeds to run and display the host specific survey, broken down by section.
	Run without options, this script saves a standard survey to $HOME/NIXserv.txt.
	-h		Help if you're lost
	-o		<path>/<name> to save. 
			Defaults to $HOME/NIXserv.txt
	
	-b		Brief survey
			Run a limited survey, without any distro or startup checks.
			Useful if you just need quick host info.
	-s		Standard Survey
			Run a survey with distro or startup checks.
			Will not do any logging checks.
	
	-v		Verbose survey
			Run a robust survey
			Include distro checks, startup checks, and logging checks.
	
	-d		When -v is specified, this sets the logging since time to be checked against
			the tiem specified VS the time the survey was ran. 
			Time is entered in 24 hour clock time.
  
### TASK LIST:
- [ ] Finish getopts loop to take any combination of options
- [ ] Finish OS/distro/kernel checks based on uname and /etc/ files
- [ ] Finish section functions so they return all command outputs
- [ ] Stylize output for ease of readability
- [ ] Test on case systems to assure accuracy and stability

### REFERENCES:
 https://github.com/dylanaraps/neofetch/blob/master/neofetch
 https://github.com/rebootuser/LinEnum/blob/master/LinEnum.sh


