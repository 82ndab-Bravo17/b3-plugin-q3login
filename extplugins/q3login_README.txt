#       q3login_README.txt
# 		Plugin for B3 (www.bigbrotherbot.com)
#       
#       Copyright 2013 d0nin380 <d0nin380<at>gmail<dot>com>
#       
#       This program is free software; you can redistribute it and/or modify
#       it under the terms of the GNU General Public License as published by
#       the Free Software Foundation; either version 2 of the License, or
#       (at your option) any later version.
#       
#       This program is distributed in the hope that it will be useful,
#       but WITHOUT ANY WARRANTY; without even the implied warranty of
#       MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#       GNU General Public License for more details.
#       
#       You should have received a copy of the GNU General Public License
#       along with this program; if not, write to the Free Software
#       Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston,
#       MA 02110-1301, USA.

Description:

    BEFORE USING THIS PLUGIN PLEASE, READ THE WHOLE README.
    
    This plugin is a modification of B3's login plugin (login.py version 1.2).
    The config file is exactly like the original login.xml.
    Purpose of this plugin is to add security to games with compromised guids
    and no client side private messaging such as CoD4.
    
    There are couple of security measures on place:
        If you type !q3login yourpassword
        the bot will check yourpassword against the password in database and if it matches
        the bot will automatically send you a new random password.
        
        If you forget the slash from /password yourpassword and end up spamming it in to the server,
        the bot will check yourpassword against the password in database and change it if needed.
        The bot will PM you the new password.
        
        These 2 arent perfectly foolproof. I often find myself hitting tab after I type password mypass
        and hit enter. If I typed pasword instead of password, this would spam my password to the server.
        Be careful with the commands and always start your password command with / so in case you have a typo
        the password wont be spammed to the server.
    

Commands:
    !q3login
        First via console: "/password yourpassword" THEN !q3login
        
        This command will log you in AFTER you type, in console: /password yourpassword
        after you run the command, you will see a message saying: "to complete authentication, type /reset password..."
        You have to type exactly "/reset password" without quotes and not "/reset what-ever-your-password-is"
        Next say event parsed will check if you reset the password to empty and restore your privileges.
        
    !q3setpassword
        First via console: "/password <newpassword>[:name]" THEN !q3setpassword
        
        This command will set your new password.
        To change password for yourself you type /password your-new-pass
        If you want to change a password to d0nin380,
        you would first set password via console: "/password newpassword:d0nin380"
        
        After you set /password, type !q3setpassword.
        Please note, you cannot have spaces in password 
        and DO NOT forget to /reset password. 
        If you don't reset password, when you connect to another server, they will be able to see it.     
        	

Installation:
	1. Unzip the content of this package into your B3 folder. It will
	place the q3login.py file in b3/extplugins and the config file q3login.xml in
	your b3/extplugins/conf folder.

	2. Open q3login.xml with your texteditor and edit to your liking.

	3. Open your B3.xml file (in b3/conf) and add the next line in the
	<plugins> section of the file:

		<plugin config="@b3/extplugins/conf/q3login.xml" name="q3login" />

	4. Restart your b3
	
Support:
	Support will ONLY be provided in http://forum.bigbrotherbot.net/releases/q3login-plugin/ so do not email me or anybody else your support questions.
	
# CHANGELOG
#   29/03/2012 - 1.0 - d0nin380
#	   * Initial Release
