Kickstart System building templates. For use with <a href="http://www.centos.org/docs/5/html/Installation_Guide-en-US/ch-kickstart2.html">Kickstart Installations</a>

ks_islandora.cfg  - Used to build an Islandora Repository server.

In your tftpboot directory on your tftpboot server issue:

	% cd /tftpboot
	% git clone git://github.com/hamhpc/kickstart.git
Make sure the rest of the installation is configure to use ks_islandora.cfg and then boot your server off your network. 


Alternatively, you can run this manually by removing the top OS installation part of the kickstart file (from %post to the top) add in a #!/bin/bash so that the file becomes a script and execute it like this:

	% cd /opt
	% git clone git://github.com/hamhpc/kickstart.git
	% cd kickstart
	# edit the file, add #!/bin/bash as the top
	% ./ks_islandora.cfg
