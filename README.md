# Ubuntu-opera-install-using-snap
opera install using snap with polish language
<br>
<br>
Files will be loacted in diffrend directory if you install browser using differend methots.
<br>
If you intalled browser using snap the file will be in directory below:
<br>
/var/lib/snapd/desktop/applications/opera_opera.desktop
<br>
If you installed browser using .deb package the files will be located in directory below:
/usr/share/applications/opera.desktop
<br>
In file you must find "Exec=. . ." and then add --lang=pl %U (you must remove "%U" behind "--lang=pl" or add "--lang=pl" behind existing "%U" beacuse there can't be two "%U" in one "Exec" command )

<br>
Exec=. . . . . . . . . . --lang=pl %U
<br>
![opera pl language snap](https://user-images.githubusercontent.com/98317764/231872780-7ba352c1-e6dc-41f7-a5bc-cb6737f0e5db.PNG)
<br>
<br>
sudo systemctl restart snapd.service
