fragroute已经很久没有更新了，我尝试在debian12下安装，依赖libevent的旧版本，而libevent又依赖python的旧版本，安装起来非常不方便。
在github上发现了ajkeeton老哥更新了一个版本解决了该问题，仓库从这里fork：ajkeeton/fragroute，以下是修改的纪录，fork它是为了方便后续自己安装软件。

At times I have needed to use or modify Dug Song's Fragroute. Figured it was due time to begin tracking those changes.

* Fragroute 1.2 uses an obsolete version of libevent and won't compile 
out-of-the-box. I've hacked around that.
* Added ability to forward the original traffic to the destination but save
  the manipulated version of the traffic to a pcap file. Doing so means nothing 
  fishy reaches the target host, but the would-be modified traffic is still saved for 
  inspection, analysis, testing, etc.
