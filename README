"""Search yum software repositories for your list of software
You can leave your /etc/yum/repos.d/ files like this:
enabled=0;
and still search them all with this program. 

The repo list is hardcoded below.  You should change to your list. 
"""

#!/usr/bin/python
import sys
import subprocess

# Simple command
#subprocess.call('ls -l', shell=True)

cmd_to_run = "yum list --enablerepo=epel --enablerepo=remi --enablerepo=rpmforge --enablerepo=atrpms --enablerepo=R-project "

i=1
for arg in sys.argv:
	if(i == 1):
		i = 0;
		print "ABOUT TO RUN THIS COMMAND:\n"
	else:
		cmd_to_run += arg

print cmd_to_run
	

subprocess.call(cmd_to_run, shell=True)
