To use ssh-agent in MacOS to remember key's passphrase, follow these steps 

1. open Terminal
2. Execute # eval 'ssh-agent'
3. Execute # ssh-agent --apple-use-keychain ~/.ssh/id_rsa
4. Edit ~/.ssh/config
```
Host my_server
  HostName 192.168.10.1
  UseKeychain yes 
  AddKeysToAgent yes
  User user_name
  Port 8202
  IdentityFile /Users/user_name/.ssh/id_rsa
```
