Live for Speed DCon 0.6R
========================


Welcome to Live for Speed - www.lfs.net


Important :
-----------
This is a special dedicated host console program for Live for Speed.

By installing this software you agree to the following :

- Live for Speed is in continual development.  Features may be
added, updated or removed at any time.  Some functional but
incomplete features may be included in order to enhance the
variety and content of the simulator.

- This software comes with no warranties of any kind.

- You install and use this software at your own risk.  The
developers of Live for Speed can not accept any responsibility for
personal injury or damage to your computer system that may arise
during the use of the software.

- The DEMO content is given to all people to use, free of charge.
The LOCKED content is for appropriately licensed users only.  You
must not make any attempt to gain access to the locked content, or
help anyone else to do so, other than by purchasing a license and
using the in-game unlocking screen.

Thank you.


Changes from DCon 0.6Q to 0.6R :
--------------------------------
New version not compatible with version 0.6Q :

Updated Blackwood race track

Fixes :

LFS could crash using /axload with a long layout name


Changes from DCon 0.6P to 0.6Q :
--------------------------------
Fully compatible - increased UDP send buffer size from 12KB to 32KB


Changes from DCon 0.6N to 0.6P :
--------------------------------
Fully compatible version - no changes in the multiplayer system


Changes from DCon 0.6M to 0.6N :
--------------------------------
Command to enable siren sound :

Allow a multiplayer guest to use siren : /cansiren username 1


Changes from DCon 0.6K to 0.6M :
--------------------------------
New version not compatible with version 0.6K :

Updated Rockingham race track
Various InSim and multiplayer updates
Text command /setlap now works in practice and qualifying
TCP position packets option now also sends TCP packets to host

Fixes :

Rare MP bug could cause LFS to enter world before track was loaded
The /track and /ws commands now accept double digit config numbers
Tracks file for /tracks command now works with double digit configs


Changes from DCon 0.6J to 0.6K :
--------------------------------
Incompatible version for new Rockingham race track
New license option for /mode command : /mode=s3


Changes from DCon 0.6H to 0.6J :
--------------------------------
Fully compatible version - no changes in the multiplayer system


Changes from DCon 0.6G to 0.6H :
--------------------------------
Incompatible version for new Westhill Circuit

InSim :

ISP_NCI packet added to give host more info about new guest

New commands :

/zero_all
- Reset all lap counters and checkpoints passed as if the race had
  just been started.  This removes checkpoints passed.
  So using this command on the first lap, before the first
  checkpoint is passed, has no effect.  After the first
  checkpoint there is an effect.  The first lap will not be
  counted.  This is intended to help with a rolling start after
  a parade lap.

/setlap username X
- X is positive : Set the lap that the user is currently on (as
  seen at the top right, not the number of laps completed).  This
  does not affect checkpoints passed.  This may help with a driver
  who reconnects after an unintended disconnection.
- X is zero : Same as the /zero_all command but for one driver.
- X is negative : subtract from the number of laps, without
  affecting checkpoints passed.  This may be useful as a penalty.


Changes from DCon 0.6F to 0.6G :
--------------------------------
InSim :

New packet IS_HCP to add extra mass or intake restrictions
to particular cars (affects all drivers using those cars)


Changes from DCon 0.6E to 0.6F :
--------------------------------
Random weather selected by default when loading a track
Message "Track loaded" now shows which track was loaded

Commands :

/exec and /wait can now take filenames with spaces in quotes
/track command (change track) accepts a weather parameter
e.g. /track BL2R 3 selects BL2R with 3rd weather


Differences in DCon compared with the old DEDI :
------------------------------------------------
- It is easier to run LFS hosts on Linux servers because fewer Windows
  functions are called.

- There is no graphical output at all, so there is no real hesitation
  or CPU usage when updating the screen with new messages.

- You can enter text using the keyboard but it is invisible while you
  type.  This is to separate stdin and stdout.

- When a player joins or leaves, some status information is output to
  the console including the selected track, a list of user names
  and the time and date.

- You can get a status message at any time by pressing ENTER without
  typing anything.


Installation :
--------------
To install the program, unzip the file into a suitable folder on your
hard drive.  You must ensure that the directory structure is preserved
by using the appropriate option in your unzip utility.  You will know
that it has been correctly unzipped if you see a data folder beside
the DCon.exe program and some more folders inside the data folder.


To run LFS DCon :
-----------------
Use a shortcut, batch file, or any method you like to start DCon.exe
with a command line.  If you do not use a command line, DCon will take
its startup options from the setup.cfg file.


Command line options :
----------------------
A command line or a command file is required for the dedicated host.
The commands are listed in Commands_DCon.txt in the docs folder.


Status file :
-------------
While your host is running, a file host63392.txt can be found in your
LFS folder, and is updated whenever the info changes :

63392 is the port number of the host.
It contains the following information:

lfs=0.6R             :version
status=ingame        :offline / online / ingame
guests=4             :current number of guests
maxguests=4          :maximum guests allowed
host=Host Name       :game name as listed on master server
pass=Optional Pass   :host password
usemaster=yes        :no / yes / hidden
trackcfg=BL1         :short name for track and config
cars=[20x"0"or"1"]   :cars allowed on host (0=no / 1=yes)
qual=0               :qualifying minutes
laps=5               :number of laps
conn=Host            :player name
conn=Guest 1         :player name
conn=Guest 2         :player name
...


Thanks :
--------
Thanks to all internet hosts for your support.


Copyright :
-----------
(c) 2002-2017 Scawen Roberts - Eric Bailey - Victor van Vlaardingen