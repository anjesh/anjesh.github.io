---
layout: post
title: Quick dirty fix to SSH Exchange Identification problem
---

TL;DR

Kill the lingering "sshd: " processes to fix the issue.

{% highlight bash %}
sudo kill $(ps aux | grep "sshd: " | grep -v grep | awk '{print $2}')
{% endhighlight %}

<hr>


I regularly get the ssh_exchange_identification errors when trying to login to our servers. 

{% highlight bash %}
A ➜  ~  ssh anjesh@zzz.com.np
ssh_exchange_identification: Connection closed by remote host
A ➜  ~  ssh anjesh@zzz.com.np
ssh_exchange_identification: Connection closed by remote host
{% endhighlight %}

Upon inspection, there are lots of lingering sshd processes. By lots, there are almost 300 such processes. 

{% highlight bash %}
anjesh@flex [~]# ps aux | grep sshd
root       474  0.0  0.0  99208  4028 ?        Ss   Feb03   0:00 sshd: root [priv]
sshd       475  0.0  0.0  67564  1628 ?        S    Feb03   0:00 sshd: root [net]
root       632  0.0  0.0  99212  4040 ?        Ss   Feb09   0:00 sshd: root [priv]
sshd       633  0.0  0.0  67564  1632 ?        S    Feb09   0:00 sshd: root [net]
root       776  0.0  0.0  97168    16 ?        Ss   Jan10   0:00 sshd: root [priv]
sshd       781  0.0  0.0  68116    12 ?        S    Jan10   0:00 sshd: root [net]
root       782  0.0  0.0  97168    16 ?        Ss   Jan10   0:00 sshd: root [priv]
sshd       783  0.0  0.0  68116    12 ?        S    Jan10   0:00 sshd: root [net]
root      1076  0.0  0.0  97168    16 ?        Ss    2014   0:00 sshd: root [priv]
sshd      1077  0.0  0.0  68116    12 ?        S     2014   0:00 sshd: root [net]
root      1476  0.0  0.0  99352  4140 ?        Ss   Feb01   0:00 sshd: root [priv]
root      1476  0.0  0.0  99352  4140 ?        Ss   Feb01   0:00 sshd: root [priv]
{% endhighlight %}

It appears that ssh_exchange_identification is due to the huge number of sshd processes. I couldn't find the reliable solution as such other than killing all of these processes. That's what I did.

I listed all the processed first, minus the process that's running that command

{% highlight bash %}
ps aux | grep "sshd: root" | grep -v grep
{% endhighlight %}

Then i extracted only the process ids

{% highlight bash %}
ps aux | grep "sshd: root" | grep -v grep | awk '{print $2}'
{% endhighlight %}
which lists only the ids

Next is easy. Kill all those processes with the following command.

{% highlight bash %}
sudo kill $(ps aux | grep "sshd: root" | grep -v grep | awk '{print $2}')
{% endhighlight %}


