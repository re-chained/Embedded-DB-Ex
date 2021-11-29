TODO:
-Add logs to a table for redundancy-
	Add grid to view logs in user admin
	Possibly create log.sqlite if it doesn't exist
?Make it so each user can only log in once
	//Add field to user table that flags them as "connected"
		-problem if unexpected closure happens (which may happen often enough to be troublesome)
		-maybe just use that flag to mark how many "connections" that user has?
*Add admin/superuser that can do user administration
	*Add ability to remove user
	Add ability to change username/password

Conceptually, here's how it could work:
At first there will be no users. On first program startup or during installation process,
admin/superuser account would need to be created. Then other accounts can be created from there.

Use root/pass to log in, all other accounts seen's passwords are their usernames.
More can be added through user admin window.

OPTIONAL:
To access tables in the program root folder the same way we do now with ARC you will need the DB browser for
sqlite3: https://sqlitebrowser.org/dl/.

Once installed to C:\Program Files or wherever you chose to install it, you should see
two different .exes: one for SQLite and one for SQLCipher. The SQLCipher one is the one you want.
Right click users.sqlite and select 'Open with.../Choose another app/Look on this PC' and choose that program. 
If you try to open any of the included database files it'll prompt you for the password.
The password for users.sqlite is just 'password'. The DB browser is a bit more feature-rich than ARC but
the basic functions are pretty easy to grasp.