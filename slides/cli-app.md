## CLI application

Usage will be

Option to login with personal OAuth token.

```bash
$ nshort --login
Enter your OAuth token: MY_OAUTH_TOKEN
You are now logged in.
```

We will save the token in a file like `~/.nshortrc`

After logging in, shorten URLs.

```bash
$ nshort http://mysuperultraverylongurl.com/withsomecomplicatedpath
http://bit.ly/jk2jkr3
```

