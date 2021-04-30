## Copy with progress bar:
```rsync -ah --progress source destination```
https://askubuntu.com/a/201250/1206522

## Get the size of contents of a folder:
```du -sh *```
https://stackoverflow.com/a/1019124/15649660

## Push the contents of colab vm to Google drive:
```
from google.colab import drive
drive.flush_and_unmount()
```
## see the correct path after remounting:
```
import os
root='/content'
os.chdir(root)
```

## Changing from gpu to cpu and vice-versa
https://stackoverflow.com/a/53267643/15649660
```
# at beginning of the script
device = torch.device("cuda:0" if torch.cuda.is_available() else "cpu")

# then whenever you get a new Tensor or Module
# this won't copy if they are already on the desired device
input = data.to(device)
model = MyModule(...).to(device)
```
