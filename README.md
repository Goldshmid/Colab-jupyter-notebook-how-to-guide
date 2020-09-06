# Colab-jupyter-notebook-how-to-guide-
This beginner's guide is written to share essential commands, tips and tricks that can be usefull when using Google Colab/Jupyter notebooks and save a lot of time.
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
