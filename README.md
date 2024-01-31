# Jersey-number-detection
Developed a ML model that provides Jersey number detection based on specific jersey colour
- Project Agenda
  - EasyOCR recognition model was trained withopen source Roboflow dataset
  - For EasyOcr training I used sagemaker Studio lab for Gpu , currently what i provied in [Ocr_training.ipynb](./main/Ocr_training.ipynb) file that same code i run in sagemaker Studilab Gpu evn
  - Then prdicted the player as a person with the help of Yolov8 pretrained "s" model as you can see in (fig-1) !["Output Image"](./runs/detect/predict/image0.jpg)
  - After detection I have done colour classification with the opencv and calculate the pixel value for blue and white colour
  - Then made a condition that satisfied if the white colour pixel value more then blue colour pixel value then only draw the box and detecte the jersey number for that player, as you can see in (fig-2) !["Output Image"](./output_image.jpg?raw=true)
  - For my custom train EasyOcr model i used only jersey number data set and i did not train any text detection model or Easyocr craft model, but for real time applycation we can train our won text detection model or we can      tain EasyOcr Craft model
  - Also I want to add one thing for player detection we can used Transfer learning with Yolov8 or any available pretrained CNN model with pytorch and tenseflow, in feature i will do the project based on this with new            problem statement. 
