# checkmk-agent-synology
Check_MK Agent for Synology DSM6

For those of you that run Check_MK, you may know that the Linux agent *does* run on our Synology's but it's a bit of an adventure getting up and running.

Thanks to the fine work at https://www.bachmann-lan.de/synology-dsm-6-check_mk-agent-paket/ and the comment section I have updated the Check_MK linux agent for my Synology running DSM6.  I thought I'd share with the community as it was a bit of a process, but know you can enjoy all my labor with a simple .SPK to install.

I couldn't have and wouldn't have done this without the fine work at bachmann-lan.de, so props should be sent there.  :)

I was inspired to do this because I started running the Check_MK 2.0.0 Beta and needed to update the agent for my Synology.  If enough people are interested I'll post updates to the 1.6.0 branch as well so you don't have to translate aus Deutsch.  :)

Installation is easy, on your DSM6 WebUI go to Package Center, click on "Manual Install" and point at the .SPK file.

You *may* need to restart the docker service (if you are runnning docker) after installation due to Docker timeouts when the mk_docker plugin tries to fetch data.  I tried everything before I gave up and kicked Docker--so you may encounter this as well.

Also, if, for some reason, you run Entware on your Syno you will have some issues with this as Entware is in this package.  Head to that URL and in the comments someone has a workaround for it.
