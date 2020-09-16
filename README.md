# Colab-jupyter-notebook-how-to-guide
This beginner's guide is written to share essential commands, tips and tricks that can be useful when using Google Colab/Jupyter notebooks and save a lot of time.
## How to upload .py files to Google Colab?
### Uploading files to the session storge (short term)
You can upload any file by dragging and dropping it from your desktop to the files menu at the left side of the screen. Since the session storge is for short term storge only,  take into consideration that the files will be deleted as you will exit Colab and your work will not be saved.
### Uploading files using Google drive (long term)
If you want to use the notebook and also be sure that every change you make is being saved, upload your file to Google drive first. Use this command to connect your Colab notebook to the drive.
```
from google.colab import drive
drive.mount('/content/drive')
```
After running this command you will need to access the presented URL link, choose your Google account and copy the authorization code you get. Past it to the requested field.
That is it! Your drive is now connected to the notebook. You can see it in the files menu on the left side of the screen.
## Useful shell commands
To check what is the current working directory, use:
```
! pwd
```
To change the working directory (for example into your google drive) use:
```
%cd /content/drive/My\ Drive
```
To clone a git repository to your working directory, get the URL link for the wanted repository first, and then use:
```
!git clone https://github.com/github_username/github_repository_name.git
```
To unzip a file from your Google "My drive" folder to your current working directory use:
```
!unzip /content/drive/My\ Drive/file.zip
```
If you want to install a specific version of PyTorch and torchvision (for example pytorch 1.6.0 and torchvision 0.7.0 torchvision with CUDA 10.1)use the next command:
```
!pip3 install torch==1.6.0+cu101 torchvision==0.7.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
```
Make sure to keep using the same CUDA version across the different libraries!

To install requirements.txt use:
```
!pip3 install -r /content/drive/My\ Drive/project_folder/requirements.txt
```
