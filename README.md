# Guglina TTS "EN"

Guglina TTS, special edition: in English (guglinatts-en), is a voice synthesizer originally designed for Brazilian Portuguese. Uses the Google Translate text-to-speech API. Read screens for the visually impaired. Transforms text into audio, allowing blind or low-vision people to access content displayed on the screen. Although the main target audience for text-to-speech conversion systems - such as Guglina TTS EN - is people with visual impairment, this type of program can be used by people with dyslexia and other reading disabilities, people with severe as well as by pre-literate children. In addition to being an assistive technology tool, voice synthesizers can still have educational and entertainment applications.
It is under the aegis of the license:
### GPLv3
> Maintainer: Felipe Facundes
###### Site: https://brasiltts.wordpress.com/
###### Blog: https://brasiltts.blogspot.com/
###### E-Mail: felipe.facundes@gmail.com
###### Telegram: https://t.me/comandos_linux
#
### Installation:

    git clone https://github.com/felipefacundes/guglinatts-en
    cd guglinatts-en
    
- **Run command:**

```
chmod +x INSTALL.sh
yes s | sh INSTALL.sh
```

##### Or manually:

``` 
sudo cp guglina*generic.conf /etc/speech-dispatcher/modules/
sudo cp speechd.conf /etc/speech-dispatcher/
sudo cp googletts* /bin/
sudo chmod +x /bin/googletts*
```

#
### Installing Dependencies:

- **The Dependencies are:**
  - espeak-ng
  - speech-dispatcher
  - orca
  - onboard
  - xsel 
  - libnotify 
  - python2-notify 
  - perl-libwww 
  - perl-www-mechanize 
  - perl-html-tree
  - ffmpeg
  - sox 
  - fmt 
  - lame 
  - perl-www-curl

#
- **Installation by ArchLinux**

```
sudo pacman -S espeak-ng speech-dispatcher orca onboard ffmpeg xsel libnotify python2-notify perl-libwww perl-www-mechanize perl-html-tree sox fmt lame perl-www-curl
```

```
sudo pacman -U svox-pico-bin-1.0+git20130326-8-x86_64.pkg.tar.xz
```

#
- **By Debian and derivatives (Ubuntu...):**
  - If you do not have pico2wave in the repository.
  - You should first convert the packages ".tar.xz" to ".deb"
  - Use the alien command to convert
  - Then just install with the dpkg command
  - **Rename** the files ".pkg.tar.xz"
  - For ".pkg.tar.gz"

```
fakeroot alien -d "nome".pkg.tar.gz
sudo dpkg -i *.deb
```

#### Fedora and derivatives: the alien also generates packages ".rpm"
    fakeroot alien -r "nome".pkg.tar.gz

#
### Finishing Installation

- Close everything and kill the session:

```
pkill -9 -u $USER
```

- Start X and type in the terminal

```
orca -s
```

- On **the tab: "Voice"**.
- Configure this way:
  - Speech system: **Speech Dispatcher**
  - Speech synthesizer: **guglina_en_tts**
  - Character: **guglina_en_tts (en)**

#
### If the onboard and orca are not booting together with the system. Include in ~/.xinitrc

``` 
onboard --not-show-in=GNOME,GNOME-Classic:GNOME --startup-delay=3.0 &
orca &
```     

- Or

``` 
cp /etc/xdg/autostart/onboard-autostart.desktop ~/.config/autostart/
cp /etc/xdg/autostart/orca-autostart.desktop ~/.config/autostart/
```

### Enabling onboard and orca is required, so that programs that have the accessibility feature, such as OKULAR, can work properly. Be sure to turn onboard! ;) ###

<br></br>

###### Guglina is an acronym of: Google + Regina. A tribute to Brazilian: Regina Bittar, responsible for Google's voice in Brazil.
#### Licença: GPLv3 ####

<br></br>

```
┏┓
┃┃╱╲ In this
┃╱╱╲╲ house
╱╱╭╮╲╲ everyone
▔▏┗┛▕▔ uses
╱▔▔▔▔▔▔▔▔▔▔╲
LINUX
╱╱┏┳┓╭╮┏┳┓ ╲╲
▔▏┗┻┛┃┃┗┻┛▕▔
--------------------------
```
