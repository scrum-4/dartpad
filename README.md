https://stackoverflow.com/questions/13023920/how-to-export-import-putty-sessions-list
putty 將設定存在 registry

與 plink 之間的關係

https://www.ssh.com/ssh/putty/putty-manuals/0.68/Chapter7.html

https://www.mainelydesign.com/blog/view/git-plink-for-ssh-on-windows

https://docswiki.newro.co/index.php/Git_setup_for_windows_using_PuTTY%27s_Plink_application_for_SSH_authentication

home/.ssh/config 設定

ProxyCommand y:/putty/plink.exe github.com %h %p
 
# for scrum-4
# url = git@github.com:scrum-4/2019wcmj.git

Host github.com
    User git
    Port 22
    Hostname github.com
 
    IdentityFile "y:\home\mdecourse\.ssh\putty_private.ppk"
 
    TCPKeepAlive yes
    IdentitiesOnly yes
    
start.bat 設定

set GIT_HOME=%Disk%:\portablegit\bin\
set GIT_SSH=%Disk%:\putty\plink.exe

最後確認近端的 private key 是取 putty 設定或 .ssh/config 中的設定