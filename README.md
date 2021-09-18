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
    ![web_scrapping full page](https://user-images.githubusercontent.com/58580347/133883623-73971b0a-362e-4676-9b07-57a93b23db78.png)
    - Output -> An image
    
    ![web_scrapping](https://user-images.githubusercontent.com/58580347/133883634-d6290d5d-80fd-466d-8571-ce5626e05073.jpg)



2. Part 2:
    - Extraction of text from the image using **Pytesseract**.
            - Pytesseract is an OCR tool in python for text recognition.
            - **OUTPUT:**
                          s
                          s

                          ERICSSON

                          In India, Ericsson has
                          trained more than
                          21,000 young people
                          in digital skills across
                          40 Learning Centres
                          
                          Readmore > ne
            
    - Object detection from the image using pre-trained **mask r_cnn model**.
            - There are many deep learning model available for object detection like R-CNN, Fast R-CNN, YOLO, SSD, etc. 
           
![segmented_object_3](https://user-images.githubusercontent.com/58580347/133883812-66acdb04-e392-4bea-8e05-76ed615634b0.jpg)
![segmented_object_1](https://user-images.githubusercontent.com/58580347/133883816-3c772bd1-ab51-4663-afa7-c247c215241a.jpg)
![segmented_object_4](https://user-images.githubusercontent.com/58580347/133883819-58aa2fe0-b300-4bc9-97c4-84ef593d7bf8.jpg)
![segmented_object_2](https://user-images.githubusercontent.com/58580347/133883821-6f2022c3-a259-4fa8-935c-68fda1076b4b.jpg)

            - Logo and call to action image is cropped manually from the image using OpenCV.
    
    
   ![web_logo_1](https://user-images.githubusercontent.com/58580347/133883829-ceb9a9eb-ce4d-4974-96b4-003bc950dbb1.jpg)

            - Text recognition of Logo using pytesseract gives the company name.
                    - **OUTPUT:**  ERICSSON
   ![web_button](https://user-images.githubusercontent.com/58580347/133883856-08ee7aba-2d4e-45cf-8192-9bb09a092e0f.jpg)

    

##### NOTE: 
1. In text recognition, there are some extra features detected like symbols.
2. Although manual cropping is not feasible, I could not find any ways to detect, so I am forced to choose manual. In my opinion, other options can be template matching (not advisable for all ads), training using the data containing logos, using pre-trained API (like google cloud vision API etc)


