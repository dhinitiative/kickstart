<H1>Kickstart System Building Templates</H1> 

<i>Note: For use with <a href="http://www.centos.org/docs/5/html/Installation_Guide-en-US/ch-kickstart2.html">Kickstart Installations</a></i>

It is assumed you already have a working Kickstart server. 

In your kickstart directory on your tftpboot server issue:

	# For a clone of all the ks templates
	% cd /tftpboot
	% git clone git://github.com/dhinitiative/kickstart.git

	# To download the templates individually
	% cd /tftpboot/kickstart
	% wget http://raw.github.com/dhinitiative/kickstart/master/ks_islandora.cfg


Make sure the kickstart server is configured to use ks_template_name.cfg and then boot your server off your network. 

<h2>Without a Kickstart Server</h2>

Alternatively, you can run these manually after the OS is installed. 
	- Remove the top OS installation part of the kickstart file (from %post to the top) 
	- Then add in a #!/bin/bash so that the file becomes a script and execute it 

	As an example:

	% cd /opt
	% git clone git://github.com/dhinitiative/kickstart.git
	% cd kickstart
	# edit the file, add #!/bin/bash at the top
	% ./ks_template_name.cfg

<hr/>

<h2><strong>List of Kickstart Templates:</strong></h2>

<a href="http://raw.github.com/dhinitiative/kickstart/master/ks_islandora.cfg"><strong><i>ks_islandora.cfg</i></strong></a>  - Used to build an Islandora Repository server.

