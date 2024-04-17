# [curl to retrieve the tarball of the latest version](https://go.dev/dl/)
``` sh
curl -OL https://golang.org/dl/go1.22.2.linux-amd64.tar.gz
```

# verify the integrity of the file you downloaded
```
sha256sum go1.22.2.linux-amd64.tar.gz
```
## Make sure checksum matches the one listed on the downloads page
![image](https://github.com/KRIISHSHARMA/go-installation/assets/86760658/a836db29-95cd-4c0f-8b69-3aa5715a4e00)

# use tar to extract the tarball
- " This command includes the -C flag which instructs tar to change to the given directory before performing any other operations. This means that the extracted files will be written to the /usr/local/ directory, the recommended location for installing Go… The x flag tells tar to extract, v tells it we want verbose output (a listing of the files being extracted), and f tells it we’ll specify a filename "

``` sh
sudo tar -C /usr/local -xvf go1.22.2.linux-amd64.tar.gz
```

# Setting Go Path 
- set Go’s root value, which tells Go where to look for its files. You can do this by editing the .profile file, which contains a list of commands that the system runs every time you log in.

``` sh
sudo vim ~/.profile
```
-  add the following information to the end of your file:

``` sh
export PATH=$PATH:/usr/local/go/bin
```
- save and exit
- refresh your profile by running the following command:

``` sh
source ~/.profile
```

- Finally Check Go version

``` sh
go version
```
![image](https://github.com/KRIISHSHARMA/go-installation/assets/86760658/9d48670d-2b44-48dd-ab06-4bc3d3e3bf59)





