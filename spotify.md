### Spotify for Linux 
This is a preview build of Spotify for Linux. As a preview release this version is still unsupported, but we're running it ourselves and will try to make sure it keeps pace with its Mac and Windows siblings.

So how do you get it? We've packaged it for Debian Squeeze/Ubuntu.

### /Ubuntu/Debian 
>Add this line to your list of repositories by editing your _/etc/apt/sources.list_

`deb http://repository.spotify.com stable non-free`

>If you want to verify the downloaded packages,you will need to add our public key

`sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 94558F59`

>Run apt-get update

`sudo apt-get update`

>Install spotify!

`sudo apt-get install spotify-client`

>above instructions taken from this link, https://www.spotify.com/us/download/previews/

>i have seen one complaint, specific to 'Debian', dependency issues with the install of libsslxxxx

### Mint only [go here] (https://github.com/two-dogs/the-kennel/blob/master/spotify-mint-install.md)

### Fedora
> Ensure ffmpeg-compat is installed, if not install it.

' rpm -qa ffmpeg-compat ' 

' sudo dnf isntall ffmpeg-compat '

> Download the repo rpm  (subsitute  fc21 and x86_64 for your fedora-release and arch if they are different)

'sudo wget -O- /etc/yum.repos.d/fedora-spotify http://negativo17.org/repos/fedora-spotify.repo ' 

>Install Spotify

`sudo dnf install spotify `

> (optional to add full local play / offline play functionality)

`sudo yum install ffmpeg ffmpeg-compat `

> `If you somehow get 'failed to import key...  run:'

> opt. 1: `gpg --import --keyserver keyserver.ubuntu.com --recv-keys 94558F59`

> opt. 2: `rpm --import --keyserver keyserver.ubuntu.com --recv-keys 94558F59`


### OpenSUSE

> Download the installer from github

`wget https://raw.github.com/marguerite/opensuse-spotify-installer/master/spotify-rpm-generator.sh`

> make it executable

`chmod +x spotify-rpm-generator.sh `

> Install Spotify (several options)
> opt. 1: `./spotify-rpm-generator.sh` ( also makes a local /home backup)

> opt. 2: `sudo rpm -ivh --nodeps spotify-*.rpm`

> opt. 3: `sudo zypper install --no-refresh --force-resolution spotify-*.rpm`
 
> (optional to add full local play / offline play functionality)

`sudo yum install ffmpeg ffmpeg-compat`

> If you recieve a gpgkey error after installing the repo rpm :

> run with --nogpg (not recommended for safety reasons  on any pkg unless you know the key and it matches t$

> i.e.  `sudo yum install spotify-client --nogpg`
> obtain the keys and reattempt

opt. 1: `gpg --import --keyserver keyserver.ubuntu.com --recv-keys 94558F59`

opt. 2: `rpm --import --keyserver keyserver.ubuntu.com --recv-keys 94558F59`
