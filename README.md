Poradnik w plikach jest do poprawy, nie działa jak będę miał czas to to naprawie 
<br>
<br>
Dostępny jest plik .zip ze wszystkimi metodami oraz przykładami
<br>
<br>
<h1> Ubuntu-opera-install-using-snap </h1>
opera install using snap with polish language
<br>
<br>
Files will be loacted in diffrend directory if you install browser using differend methots.
<br>
<br>
<h2> "apt" and ".deb packages" </h2>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If you intalled browser using snap the file will be in directory below:
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; /var/lib/snapd/desktop/applications/opera_opera.desktop
<br>
<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If you installed browser using .deb package the files will be located in directory below:
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; /usr/share/applications/opera.desktop
<br>
<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If you installed browser using flatpack you need to fallow instruction below:
<br>
<br>
In file you must find "Exec=. . ." and then add "--lang=pl %U" at the end of the line
<br>
after that you must remove "%U" from behind the "--lang=pl" or add "--lang=pl" behind existing "%U" beacuse there can't be two "%U" in one "Exec" command line
<br>
<br>
<br>
This is example of the right one
<br>
<br>

![example2](https://user-images.githubusercontent.com/98317764/232561334-ca5efd9e-aaf8-40a1-a727-e78fac82dce8.PNG)
<br>
This is example of the bad one
<br>

![example1](https://user-images.githubusercontent.com/98317764/232560992-fc811ad9-02e0-4837-b504-36afcc2e4dcc.PNG)
<!--[opera pl language snap](https://user-images.githubusercontent.com/98317764/231872780-7ba352c1-e6dc-41f7-a5bc-cb6737f0e5db.PNG)-->
<br>
<h2> Flatpack </h2>
<br>
First you need to install flatpack and Opera
<br>
Flatpack install
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sudo apt install flatpak
<br>
Opera install
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; flatpak install flathub com.opera.Opera
<br>
next you need to veryfiy that opera was installed sucessfully
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; flatpak list | grep opera
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <!--this is output if opera was installed sucessfully-->
<br>
<br>
Finally you change language using this command
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; flatpak override com.opera.Opera --env=LANG=pl.UTF-8
<br>
after that you sucessfully changed language in opera
