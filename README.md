# cloudwatch-monitoring-scripts
CloudWatch Monitoring Scripts for Amazon EC2


Updated mon-put-instance-data.pl file to add an option --mem-avail-incl-sreclaimable 

if you go by this kernel commit which is merged at 3.14, it clearly says the mem available includes sreclaimable. Hence adding an option --mem-avail-incl-sreclaimable to include sreclaimable into memory utilization calculation.
Until 3.14 kernel there is no metric called memAvailable in /proc/meminfo. 
https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=34e431b0ae398fc54ea69ff85ec700722c9da773
