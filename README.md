# radio-crontab
To record programmes from radio stations, by parsing the programmes time-table, and generating timed crontab lines

Rádióműsorok rögzítésére való Ruby script program.

A rögzíteni kívánt műsorok címét és/vagy alcímét a mellékelt .json fájlban kell megadni, felsorolni.

A program elemzi a rádiócsatorna műsorújságját, pl reguláris kifejezések segítségével (vagy esetleg a Nokogiri is használható),
ezzel megállapítja a rögzítésre megjelölt, rögzíteni kívánt műsorok kezdési időpontját, valamint azok hosszát. Ennek
megfelelően Linux "crontab" bejegyzéseket állít elő egy my-crontabs.txt fájlban. Ezt kell hozzáadni a crontab-unkhoz: 
fcrontab my-crontabs.txt  

Jelen állapotában csak Linux operációs rendszerrel működik. Javítgassátok.
Szükséges hozzá az ffmpeg és a curl programok telepítése.
A crontab "fcrontab / fcron" változatával, implementációjával használható: https://github.com/yo8192/fcron

