##Virtual machine Setup instructions:

VM disk images of Centos 7.1 can be downloaded from https://download.gluster.org/pub/vmimages  

####For KVM users:
- Copy this image four times (or clone).  
- Create a new VM by importing the 4 disk images copied.  
- Boot the VMs, verify if both have IP addresses assigned and can ping each other.  

####For Virtual Box users:
- Copy the vdi image and create a new VM by importing the copied image.  
- Change network type to host-only or internal  
- Clone VM (Reinitialize MAC) linked clone for faster clone  

Add the following for ease of use:  
* Passwordless ssh access to your system  
  ```# ssh-keygen -t rsa```  
  Copy the contents of ~/.ssh/id_rsa.pub on your host, to the ~/.ssh/autherized_keys on your guest

* Hostname for all the VMs  
  Set the hostname  
  ```# hostnamectl set-hostname vb1```

  Setup hostname-ip mapping. Add entry for each VM in /etc/hosts  
  ```E.g:
  192.168.58.101   vb1
  192.168.58.102   vb2
  192.168.58.103   vb3
  ```

Once the VMs are booted with the above said network configurations, they are all set for Gluster setup. The tutorial will have a live demo for setting up and troubleshooting Gluster.  


For future references below are the links to recorded demo:  
* [Create trusted storage pool](https://asciinema.org/a/8orgv7dv0nusgqw67cid6fuws)
* [Create distribute vol](https://asciinema.org/a/bzkamg6rdgva2s1ft5e3uaw5w)
* [Create replicate vol](https://asciinema.org/a/97zrqc28k18jf227hgj9cfsc9)
* [Create distribute replicate vol](https://asciinema.org/a/evb35a1muv6uamojcvdz0327a)
* [Create Disperse vol](https://asciinema.org/a/63ucy7se7d3b74j9h4hrqtvgo)
* [Create Distribute Disperse vol](https://asciinema.org/a/eq23v5goggopnk23ihzajr02b)
* [Create Shard vol](https://asciinema.org/a/55191587nx1hvwhvtrpoxh6gm)
* [Delete any vol](https://asciinema.org/a/05h33wz51eelevdtpfi3paucx)
* [Expand any distribute vol](https://asciinema.org/a/4vu6h12v8o77fc0mwukvlgxzb)
* [Shrink any distribute vol](https://asciinema.org/a/7anfxwrh5yfgyg8zb7hjo7tkc)
* [Access Mechanism, FUSE](https://asciinema.org/a/7gml2w9fgos30562e1cbo85be)
* [Access Mechanism, SMB](https://asciinema.org/a/3b3pk46fwsvlo4aul7fxndmn8)
