# Go-fiddle
We run Go [^1] (programming language) on Arch.
## Steps to run Go (w/ GVM) on Arch 
First, we prepare ourselves by installing Bison for potential compilation.  
```
sudo pacman -S bison
```  
Then we proceed with GVM [^2] (Go Version Manager) installation.  
```
bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
```
Finally, we install Go as follows (-B flag installs ready binary).
```
gvm install go1.4
gvm install go1.4 -B
```
Then you set `version as default`, `list installed go versions`, `install new version` and ultimately `set new as default`.
```
gvm use go1.4 --default
gvm list
gvm install go1.24.0
gvm use go1.24.0 --default
```


## (Install temporary Go in system for Go's (source via GVM) compilation)
You might need to install Go into Arch in order to compile downloaded Go versions via GVM.  
This is accomplished by these 3 commands:  
```
sudo pacman -S go
gvm install go1.4
sudo pacman -Rns go
```
NOTE: I bypassed this error by flagging `-B` because I was facing compilation errors on my Arch installation.


[^1]: https://go.dev/
[^2]: https://github.com/moovweb/gvm
