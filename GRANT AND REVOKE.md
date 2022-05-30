# DATA CONTROL LANGUAGES

    Can manipulate the privileges of database users. Uses 2 commands, [grant] and [revoke].

## HOW TO CREATE / SELECT A USER

    	select user (); (Displays current user)
    	select host, user from mysql.user; (View all users)
    	create user '[username]'@'host' IDENTIFIED BY '[password]'; (Creates a new user)

### GRANT

    	Enables admins to grant privileges and roles, which can be granted to user accounts.
    		SYNTAX:
    			-A grant statement can only grant a role OR a privilege, not both.
    			- ON distinguises whether the a privilege or a role is granted.
    				-Having ON grants a role
    				-Not having ON grants a privilege
    			-A user can have both a privilege and a role, but two different grants must be used
    	 grant all privileges on *.* to [new.user]@localhost; (Grants all privileges to a user)
    	 In order to have the new privileges take effect without needing to restart, use the command
    		flush privileges;

### PRIVILEGES THAT CAN BE GRANTED

    	CREATE - allows users to make a database or table
    	SELECT - allows users to retrieve data
    	INSERT - allows users to add new entries into a table
    	UPDATE - allows users to modify the contents in a table
    	DELETE - allows users to erase table entries
    	DROP - -allows users to delete tables or databases

    	grant create, select on *.* to [user]@localhost; (Grants specific privileges)

    	revoke all privileges on *.* from [user]@localhost; (Revokes privileges)

    	DROP USER [user]@localhost; (Deletes a user)

    	show grants for [user]@localhost; (Shows the grants for that user)
