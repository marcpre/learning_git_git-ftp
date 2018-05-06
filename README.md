# learning_git_git-ftp

## Install

### Windows

Run the following as `admin`:
```
curl https://raw.githubusercontent.com/git-ftp/git-ftp/master/git-ftp > "C:\Program Files (x86)\Git\bin\git-ftp"
chmod 755 "C:\Program Files (x86)\Git\bin\git-ftp"
```

[Installation Instructions](https://github.com/git-ftp/git-ftp/blob/master/INSTALL.md)
[Git Url Windows ](https://stackoverflow.com/questions/50197203/using-curl-with-windows-path)

### Config git-ftp

```
# Setup
git config git-ftp.url "ftp://ftp.www323.your-server.de:21/public_html"
git config git-ftp.user "xxxx"
git config git-ftp.password "xxxx"

# Upload all files
git ftp init

# Or if the files are already there
git ftp catchup

# Work and deploy
echo "new content" >> index.txt
git commit index.txt -m "Add new content"
git ftp push
# 1 file to sync:
# [1 of 1] Buffered for upload 'index.txt'.
# Uploading ...
# Last deployment changed to ded01b27e5c785fb251150805308d3d0f8117387.
```

[Configure git-ftp](https://github.com/git-ftp/git-ftp)
