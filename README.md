# AdEase_ml_intern_task

### Task:
1. Write a Python program to scrape display ads from a webpage.
2. Write a Python program to extract the follow from the scraped ad:
    - logo
    - text
    - call to action button
    - product image (or) any image, if any
    - background image

- The above task is solved using python in Jupyter Notebook.

1. Part 1:
    - Scraping of an display ad from the website is done using **BeautifulSoup** and **Selenium**.
    - Output -> An image

2. Part 2:
    - Extraction of text from the image using **Pytesseract**.
            - Pytesseract is an OCR tool in python for text recognition.
    - Object detection from the image using pre-trained **mask r_cnn model**.
            - There are many deep learning model available for object detection like R-CNN, Fast R-CNN, YOLO, SSD, etc.
    - Logo and call to action image is cropped manually from the image using OpenCV.
    - Text recognition of Logo using pytesseract gives the company name.

NOTE: 
    1. In text recognition, there are some extra features detected like symbols.
    2. Although manual cropping is not feasible, I could not find any ways to detect, so I am forced to choose manual. In my opinion, other options can be template matching (not advisable for all ads), training using the data containing logos, using pre-trained API (like google cloud vision API etc)


