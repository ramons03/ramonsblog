title: ffmpeg
author: Ramon Sanchez
author_id: ramons
language: en-US
date: 2017-07-09 02:36:24
tags:
---
[FFmpeg](https://en.wikipedia.org/wiki/FFmpeg) is a free software project that produces libraries and programs for handling multimedia data. FFmpeg includes libavcodec, an audio/video codec library used by several other projects, libavformat (Lavf), an audio/video container mux and demux library, and the ffmpeg command line program for transcoding multimedia files. FFmpeg is published under the GNU Lesser General Public License 2.1+ or GNU General Public License 2+ (depending on which options are enabled).

The name of the project is inspired by the MPEG video standards group, together with "FF" for "fast forward". The logo uses a zigzag pattern that shows how MPEG video codecs handle entropy encoding.


### Installing
Instructions from [vultr](http://bit.ly/2sTIy7P)  

1. Update the system  
  
  ```sh
  sudo yum install epel-release -y
  sudo yum update -y
  sudo shutdown -r now
  ```

2. Install the Nux Dextop YUM repo  
 
  There are no official FFmpeg rpm packages for CentOS for now. Instead, you can use a 3rd-party YUM repo, Nux Dextop, to finish the job.
 
    * On CentOS 7, you can install the Nux Dextop YUM repo with the following commands:
      ```sh
      sudo rpm --import http://li.nux.ro/download/nux/RPM-GPG-KEY-nux.ro
      sudo rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm
       ```
    * For CentOS 6, you need to install another release:
      ```sh
      sudo rpm --import http://li.nux.ro/download/nux/RPM-GPG-KEY-nux.ro
      sudo rpm -Uvh http://li.nux.ro/download/nux/dextop/el6/x86_64/nux-dextop-release-0-2.el6.nux.noarch.rpm
      ```

3. Install FFmpeg and FFmpeg development packages
  ```sh
  sudo yum install ffmpeg ffmpeg-devel -y
  ```
4. Test drive
  1. Confirm the installation of FFmpeg:  
    ```sh
    ffmpeg
    ```
    This command provides detailed info about FFmpeg installed on your system. At the time of writing, the version of FFmpeg installed using Nux dextop is 2.6.8.     
    If you want to learn more about FFmpeg, input:  
    ```sh
    ffmpeg -h
    ```
  2. Convert an mp3 audio file to an ogg audio file.  
    You need to determine the appropriate parameters when using FFmpeg. For example, you can convert an mp3 file to an ogg file using the following commands:
    ```sh
    cd
    wget https://archive.org/download/MLKDream/MLKDream_64kb.mp3
    ffmpeg -i MLKDream_64kb.mp3 -c:a libvorbis -q:a 4 MLKDream_64kb.ogg
    ```
  3. Convert an flv video file to an mp4 video file.  
  
    Here is an example of lossless conversion from flv to mp4:  
    
    ```sh
    cd
    wget https://archive.org/download/beeenieilp/beeen.flv
    ffmpeg -i beeen.flv -y -vcodec copy -acodec copy beeen.mp4
    ```

#### ffmpeg cheatsheets
* [audio and video](http://bit.ly/2sTgdhE)
* [video to gif](http://bit.ly/2sTqGd5)
* [resize and scale](http://bit.ly/2sTjwpj)