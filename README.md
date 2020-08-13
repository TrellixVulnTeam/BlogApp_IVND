# BlogApp
A blooging application with Kivy
All the requirements for executing the code is provided in the requirement.txt

To start the application we execute main.py

A point to remember is that I have used the absolute path of the files and directories instead of the relative path. I
possible that there might be error when executed on another machine due to the differences in file and directories stored
locations.

The app has the following screens:
1. LoginWindow
    We log in through this app. We can visit as a guest as well but the guest can only view public posts and nothing
    else. There is a button to direct us to the signup window

2. CreateAccountWindow
    It gets the basic credentials and creates an account

3. HomeWindow
    It contails buttons that direct us to other windows that perform the bsic operartions of a blog. The buttons are:
        - Post (to create new posts)
        - Update Post (to view owned posts and edit them)
        - All Post (to see all public posts)
        - Shared with me (to see posts that are shared with the user)
        - Log out (to log out)

4. PostWindow
    The post window is where we create our posts. The posts can either be private (no one can see it) or public or even
    share it with specific individuals. The additions button in it will allow us to upload images or videos or audios.

5. MyWindow
    This window displays all the posts that are owned by the user. We can select one post and either update or delete
    it.

6. UpdateWindow
    We can update our owned post through this window.

7. AllWindow
    This window will allow us to see all the posts that are public. We can also select one of the posts and view it in
    detail.

8. View Window
    This window displays the contents of the post that was selected for viewing.

9. SharedWindow
    This window allows us to see the posts that are shared with us. We can also select one of the posts to read it in
    detail.

10.Additions Window
    We can upload multimedia files through this window. One drawback is that there is no file choosed and we will have
    to povide the locations of the files manually. We should also make sure or slashes in the file path are "/" and not
    "\". If we are not providing any file say video we must ensure that its textbox is empty (without the displayed text)
    before uploding.

The selectable lists that display our posts is achieved by using Recycle View as kivy does not support list view like
it did before.

All data is stored in two files. One a normal file while the other is encrypted. All encrypted files start with an "e".
Every action in the app is logged in the log.txt file while its encrypted version is stored in elog.txt. Encryption is
done using the cryptography package. The cryptographic technique used id the Fernet encryption technique.