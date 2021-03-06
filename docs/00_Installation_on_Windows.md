
[Edit this page](https://github.com/serut/doc-vieassoc/edit/master/docs/00_Installation_on_Windows.md)

## File installation
Install the github windows software.
Then, click on tools > options.
![](img/1.png "tools > options")
change the default storage directory to point to the webserver root.
![](img/1-5.png "Default storage directory")
Fork the [Vie Associative](https://github.com/serut/vieassociative) repository and clone the code on your computer.

## Database installation

Create a database with PhpMyAdmin.
![](img/2.png "Create a database")
Open the file web_server_root/your_vieassoc_folder/**app/config/database.php** and update the database password and the database name with your local credentials
![](img/2-5.png "local credentials")

## Host file configuration
It allows you to reach the website with an other URL than localhost. You will use **.vieassoc.lo**
The file is located on YOUR_SYSTEM_LETTER:\Windows\System32\Drivers\etc and the file is **hosts** .
![](img/3.png "YOUR_SYSTEM_LETTER:\Windows\System32\Drivers\etc")
On W8, you may need a trick in order to edit the file because it is protected : copy paste this file anywhere else than the system's folder, edit it, and replace it where you found it.
Add this to the hosts file:
	
	127.0.0.1 www.vieassoc.lo
	127.0.0.1 association.vieassoc.lo


## Apache VirtualHost configuration
The location of this apache file depends on your Web server. For Xampp, it's YOUR_XAMPP_FOLDER\apache\conf\extra, and you will need to edit **httpd-vhosts.conf**
After editing, your file should contain ( don't forget to fill with correct values ) : 

	NameVirtualHost *:80
	<VirtualHost www.vieassoc.lo:80>
	    DocumentRoot "YOUR_XAMPP_LETTER:/xampp/htdocs/your_folder/public"
	</VirtualHost>
	<VirtualHost association.vieassoc.lo:80>
	    DocumentRoot "YOUR_XAMPP_LETTER:/xampp/htdocs/your_folder/public"
	</VirtualHost>

## Environment variables in Windows

For the next step, you'll need to execute a program written in php. But first, we will configure environment variables in Windows in order to specify the directory where the php executable is located.

- From the Desktop, right-click My Computer and click Properties.
- Click Advanced System Settings link in the left column.
- In the System Properties window click the Environment Variables button.

![](img/5.png "local credentials")
More information [here](http://www.computerhope.com/issues/ch000549.htm)

Edit the **system** environment variable ( not user environment variable ) nammed "Path" and add to the previous value 
- a semicolon ;
- then the folder where php.exe is located (I guess in your case that would be C:\xampp\php )

"Path" would looks like [precedent values of path];C:\xampp\php

## Database deployement
Hold the SHIFT key while you right-click the Windows window on the vieassociative root folder. You should see "Open Command Window here"

1. On the command window, type : 

    	php artisan migrate --env=local


##That's it
You can try to reach your local website now : [http://www.vieassoc.lo](http://www.vieassoc.lo)

##Warning
At this point, Vie Associative is not completly functionnal, because you need to specify some password for using specific functionnalities : Amazon Upload File, Oauth connection, Pubnub notification ...
You can find on the prod config directory a lot of getenv(). You need to setup **system** environment variable ( not user environment variable )

	Missing :
	VA_DB_HOST
	VA_DB_NAME
	VA_DB_USERNAME
	VA_DB_PASSWORD
	VA_SMTP_PASSWORD
	VA_APP_KEY
	...