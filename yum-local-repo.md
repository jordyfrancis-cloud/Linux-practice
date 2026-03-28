This is a simple tasks to create yum repositories using an ISO image
 check for the image using lsblk
 then mount /dev/cdrom /mnt
 ls /mnt

 vi /et/yum.repos.d/lcoal.repo
  [BaseOS]
  name=BaseOS
  baseurl:file:///mnt/BaseOS
  gpgcheck=0
  enabled=1


  [AppStream]
  name=AppStream Repo
  baseurl=file:///mnt/AppStream
  enabled=1
  gpgcheck=0
  save it using :wq!

  then dnf clean all

  dnf repolist
