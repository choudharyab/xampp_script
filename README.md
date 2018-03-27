# xampp_script

1.Creating a script to stat XAMPP automatically
 
   a.First in the terminal type following command:
          sudo gedit /etc/init.d/lampp     ##creates and opens the necessary script file.

   b.After typing above command the text editor will open and write following code in that terminal
			 #!/bin/bash
			### BEGIN INIT INFO
			# Provides: lampp
			# Required-Start:    $local_fs $syslog $remote_fs dbus
			# Required-Stop:     $local_fs $syslog $remote_fs
			# Default-Start:     2 3 4 5
			# Default-Stop:      0 1 6
			# Short-Description: Start lampp
			### END INIT INFO
			/opt/lampp/lampp start

	c.Save the file and to need to provide permission to make file exectuable.

			$ls –l /etc/init.d/lampp        ##lists the current file attributes.

			$sudo chmod +x /etc/init.d/lampp  ##adds the execute permission in file attributes.
			$ls –l /etc/init.d/lampp          ##verifies the execute permission has been successfully added in file attributes.

   d.Now run following command 
          $sudo update-rc.d lampp defaults 
          
  ##This command instructs Ubuntu to check and run our custom script file in default runlevels.
