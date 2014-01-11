Kickstart System building templates. For use with <a href="http://www.centos.org/docs/5/html/Installation_Guide-en-US/ch-kickstart2.html">Kickstart Installations</a>

It is assumed you already have a working Kickstart server and the ks_.cfg file can be cloned to that location for server building. 


In your tftpboot directory on your tftpboot server issue:

	% cd /tftpboot
	% git clone git://github.com/hamhpc/kickstart.git


Make sure the kickstart server is configured to use ks_.cfg and then boot your server off your network. 

<h3><strong>List of Kickstart Templates:</strong></h3>

<i>ks_islandora.cfg</i>  - Used to build an Islandora Repository server.

Alternatively, you can run them manually by removing the top OS installation part of the kickstart file (from %post to the top) add in a #!/bin/bash so that the file becomes a script and execute it like this:

	% cd /opt
	% git clone git://github.com/hamhpc/kickstart.git
	% cd kickstart
	# edit the file, add #!/bin/bash as the top
	% ./ks_islandora.cfg
