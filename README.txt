TODO:
Add logs to a table for redundancy
Make it so each user can only log in once
Add admin/superuser that can do user administration
	Add ability to remove user
	Add ability to change username/password

As of now log ins/log outs are tracked in log.txt. It will append any log ins/outs to that file,
or create it and start over if it doesn't exist.


Conceptually, here's how it could work:
At first there will be no users. On first program startup or during installation process,
admin/superuser account would need to be created. Then other accounts can be created from there.


Username/Passwords already present in users.sqlite are:
root	pass
root1	pass1
test1	test1
test2	test2

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