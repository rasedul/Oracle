# abc-aid of life#
Hello,
I face a problem when I use command in terminal(CentOS 7) as yum install epel-release.Then exicute below:
loaded plugins: fastestmirror, priorities
Existing lock /var/run/yum.pid: another copy is running as pid 12616.
Another app is currently holding the yum lock; waiting for it to exit…
The other application is: yum-updatesd-he
Memory : 14 M RSS ( 26 MB VSZ)
Started: Tue Aug 9 08:19:02 2016 – 14 day(s) 11:47:39 ago
State : Sleeping, pid: 12616
....and continue these same messages.
# I fix this situation #
Open terminal and type
yum install samba [Login must root&localhost]
for to confirm about sleeping, pid:12616
then type
ps aux | grep yum
and sample output: many line....like last: grep--color=auto yum.
Now simply kill the PID using command:
kill -9 12616
So go ahead and start using the first yum command like yum install epel-release
done successfully complete,then type
yum update
done successfully update.
So, enjoy everyone,
Thankyou
