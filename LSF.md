Conversation opened. 1 read message.

Skip to content
Using Gmail with screen readers
harsha 
3 of 29
DataStage

Rahul Mohan <rahulraul03@gmail.com>
Attachments
Mon, Sep 5, 2022, 10:38 AM
to harsha98e

Hi Harsha,

I have prepared a few documents for DataStage. Please go through it and let me know if any changes are required. Thanks! 

Mob: +91-9962496116
Email: rahulraul03@gmail.com

 5 Attachments
  •  Scanned by Gmail
Compose:
New Message
MinimizePop-outClose
harsha98e@gmail.com. Press tab to insert.
** LSF Commands **

$lsfstartup
$lsfshutdown

$badmin hopen
$badmin hclose

$badmin hstartup
$lsadmin limstartup
$lsadmin resstarup

$badmin hshutdown
$lsadmin limshutdown
$lsadmin resshutdown

After editing the file, run $lsadmin reconfig & $badmin mdbrestart to apply the changes.

$profile.lsf - Profile file for the lsf
$lsf.shared - It stores the versions and the types of hardware
$lsf.cluster.prod11712 - It contains admin of lsf user id and the cluster server names
$lsf.conf - lsf configuration(folders and every other param is defined here)
$lsb.hosts - We define the lsf hosts the maximum no. of jobs that can be run on each node.
$lsb.queues - It defines the queues and their settings(small_low, small_high, large_low, large_high)
$lsb.params - It is used to set the params before a job is submitted to the hosts.

Use the lsid, badmin, bparams & lsclusters commands to find the information about the lsf cluster. 

$bhosts
$bparams
$badmin
$lsclusters
$bqueues

LSF.txt
Displaying LSF.txt.
