# install-git
Set up the latest git version on different Linux distro  
Source code from https://github.com/git/git/archive/v2.25.0.tar.gz

## Manual install on centos
log in as a normal user on your centos minimal  
```shell script
  cd
  git
  sudo yum -y update
  sudo yum -y install wget 
  wget  https://github.com/git/git/archive/v2.25.0.tar.gz
  tar -zxvf v2.25.0.tar.gz 
  cd git-2.25.0
  sudo yum -y install "@Development tools"
  sudo yum -y install gettext-devel curl-devel perl-CPAN perl-devel openssl-devel zlib-devel
  git  --version 
  make configure 
  ./configure --prefix=/usr/local
  nproc    # display the number of core 
  make -j<value of nproc>
  make -j<value of nproc> test 
  git --version 
  sudo yum -y remove git 
  git --version 
  sudo make install 
  git --version 
  source ~/.bash_profile 
  git --version 
``` 
