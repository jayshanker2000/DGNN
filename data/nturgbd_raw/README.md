For NTU data, visit the follwing link:
https://github.com/shahroudy/NTURGB-D

Copy the follwoing two files in your drive then download it, otherwise the Download limit will be reached and the connection will reset after 24 hours:
All files are in zip format...

https://drive.google.com/open?id=1CUZnBtYwifVXS21yVg62T-vrPVayso5H - 6GB

https://drive.google.com/open?id=1tEbuaEqMxAV7dNc4fqu1O4M7mC6CJ50w - 4GB



When the data is generated, it is stored in Colab VM and not on the Drive. To save it on drive, run the below cell:
```
from google.colab import drive
drive.flush_and_unmount()
```
But you need to remount the drive:
```
from google.colab import drive
drive.mount('/content/drive')
```
Then you are unable to navigate through colab commands e.g. cd, ls, pwd. To fix:
```
import os
root='/content'
os.chdir(root)
```
