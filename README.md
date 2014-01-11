<H1>Kickstart System Building Templates</H1> 

<i>Note: For use with <a href="http://www.centos.org/docs/5/html/Installation_Guide-en-US/ch-kickstart2.html">Kickstart Installations</a></i>

It is assumed you already have a working Kickstart server and the ks_template_name.cfg files can be cloned to that location for server building. 

In your tftpboot directory on your tftpboot server issue:

	% cd /tftpboot
	% git clone git://github.com/hamhpc/kickstart.git


Make sure the kickstart server is configured to use ks_template_name.cfg and then boot your server off your network. 

<h2>Without a Kickstrt Server</h2>

Alternatively, you can run them manually after the OS is installed. 
	- Remove the top OS installation part of the kickstart file (from %post to the top) 
	- Then add in a #!/bin/bash so that the file becomes a script and execute it 

	As an example:

	% cd /opt
	% git clone git://github.com/hamhpc/kickstart.git
	% cd kickstart
	# edit the file, add #!/bin/bash as the top
	% ./ks_template_name.cfg

<hr/>

<h2><strong>List of Kickstart Templates:</strong></h2>

<strong><i>ks_islandora.cfg</i></strong>  - Used to build an Islandora Repository server.

