Qubritics-Selection-Assignment
###### <b>Task # 02:</b> 
<h1>Computer Vision(OCR/ICR):</h1>

### Go to https://content.sbigeneral.in/uploads/e1904ff17d084f6582d5cc43bb6e059e.pdf

<ul>
<li>Perform OCR on handwritten text using the above form</li>
<li>Print the given form.</li>
<li>Fill it with handwritten data.</li>
<li>Apply OCR via OpenCV.</li>
</ul>

## <b>Step-1: Installing extra Required Libraries</b>
install libraries 'tesseract-ocr' and 'pytesseract'<br>
<code>!apt install tesseract-ocr</code><br>
<code>!pip install pytesseract</code>

## <b>Step-2: Importing required Libraries</b>
import all libraries.<br>


<code>import os, cv2, shutil, random, pytesseract</code><br>
<code>import numpy as np</code><br>
<code>from google.colab import files</code><br>
<code>from google.colab import drive</code><br>
<code>import matplotlib.pyplot as plt</code><br>
<code>try:</code><br>
<code> from PIL import Image</code><br>
<code>except ImportError:</code><br>
<code>  import Image</code><br>


## <b>Step-3:Mounting Google Drive to access the required files</b>
mount google drive.<Br>
<code>drive.mount('/content/gdrive',force_remount=True)</code><br>

## <b>Step-4: Setting path for Images so that the files can be directly used</b>
<code>drive.mount('/content/gdrive',force_remount=True)</code><br>
## <b>Step-6: Accesing image from path & Displaying via __</b> *Plt.Show()*
<code>image_path = '/content/gdrive/MyDrive/Computer Vision Qubritics Tasks/Text extraction using OCR/Images/1.jpg'</code><br>
  
##### Step-5:<Br>
Read an image and display it.<br>
<code>image_orignal=cv2.imread(image_path)</code><Br>
<code>plt.imshow(image_orignal)</code><Br>
<code>plt.axis("off")</code><Br>
<code>plt.show()</code><Br>
  
## <b>Step-8: Applying Tesseract_OCR Text Extraction on Orignal image</b>
Let extract text using tesseract module.<Br>
<code>image_path_in_colab=image_path</code><br>
<code>extractedInformation = pytesseract.image_to_string(Image.open(image_path_in_colab))</code><br>
<code>print(extractedInformation)</code><br>
  
##### FootNote:
<h5> The system accuracy is lower due to LOW-IMAGE-QUALITY!</h5>
