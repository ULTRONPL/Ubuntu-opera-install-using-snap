# Ubuntu-opera-install-using-snap
opera install using snap with polish language
<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Files will be loacted in diffrend directory if you install browser using differend methots.
<br>
&nbsp<space><space><space> If you intalled browser using snap the file will be in directory below:
<br>
/var/lib/snapd/desktop/applications/opera_opera.desktop
<br>
If you installed browser using .deb package the files will be located in directory below:
/usr/share/applications/opera.desktop
<br>
In file you must find "Exec=. . ." and then add --lang=pl %U at the end of the line
<br>
you must remove "%U" behind "--lang=pl" or add "--lang=pl" behind existing "%U" beacuse there can't be two "%U" in one "Exec" command
<br>
This is example
the right one
![example2](https://user-images.githubusercontent.com/98317764/232561334-ca5efd9e-aaf8-40a1-a727-e78fac82dce8.PNG)
<br>
the bad one
![example1](https://user-images.githubusercontent.com/98317764/232560992-fc811ad9-02e0-4837-b504-36afcc2e4dcc.PNG)
<br>
<br>
![opera pl language snap](https://user-images.githubusercontent.com/98317764/231872780-7ba352c1-e6dc-41f7-a5bc-cb6737f0e5db.PNG)
<br>
<br>
sudo systemctl restart snapd.service
