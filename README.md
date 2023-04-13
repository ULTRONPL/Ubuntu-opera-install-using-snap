# Ubuntu-opera-install-using-snap
opera install using snap with polish language
<br>
<br>
sudo nano /var/lib/snapd/desktop/applications/opera_opera.desktop
<br>
<br>
Exec=......... /usr/bin/snap run opera --lang=pl %U
<br>
![opera pl language snap](https://user-images.githubusercontent.com/98317764/231872780-7ba352c1-e6dc-41f7-a5bc-cb6737f0e5db.PNG)
<br>
<br>
sudo systemctl restart snapd.service
