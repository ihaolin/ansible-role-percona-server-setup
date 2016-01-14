percona-server-setup
=========
Install **percona server** on remote host.

Requirements
------------

None.

Role Variables
--------------
	
	# defaults/main.yml
	
	# the db user group
	USER: mysql
	
	# the db user
	GROUP: mysql
	
	# installed path
	INSTALL_PATH: /mnt/mysql
	
	# cmake file version
	CMAKE_VERSION: 2.8.11.2
	
	# cmake file
	CMAKE_FILE: http://pkgs.fedoraproject.org/repo/pkgs/cmake/cmake-{{CMAKE_VERSION}}.tar.gz/6f5d7b8e7534a5d9e1a7664ba63cf882/cmake-{{CMAKE_VERSION}}.tar.gz
	
	# percona server version
	PERCONA_SERVER_VERSION: 5.6.27-76.0
	
	# percona server tar url
	PERCONA_SERVER_FILE: https://www.percona.com/downloads/Percona-Server-5.6/Percona-Server-{{PERCONA_SERVER_VERSION}}/source/tarball/percona-server-{{PERCONA_SERVER_VERSION}}.tar.gz

Dependencies
------------

None

Example
----------------

+ The **``Playbook``** like:

		- hosts: myhost
		  roles:
		  	 - role: ihaolin.percona-server-setup
		  	   USER: mysql
		  	   GROUP: mysql
		  	   INSTALL_PATH: /mnt/mysql
		  	   CMAKE_VERSION: 2.8.11.2
		  	   CMAKE_FILE: http://... 
		  	   PERCONA_SERVER_VERSION: 5.6.27-76.0
		  	   PERCONA_SERVER_FILE: http://... 		  	   
		  	   
		    


License
-------

MIT

Author Information
------------------

[haolin.h0@gmail.com](mailto:haolin.h0@gmail.com)