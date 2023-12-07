# CV Super Resolution Python Project

## 1. Models
### SRCNN
![SRCNN](https://github.com/YuanrunXu/USC-EE541-Final-Project-Super-Resolution/assets/43257371/f506a4a8-80fb-47e6-8c55-739181e1a53f)

### SRGAN
![SRGAN](https://github.com/YuanrunXu/USC-EE541-Final-Project-Super-Resolution/assets/43257371/1796abc7-d63a-4d80-ab4e-307d54404e05)


## 2. Training curves
### SRCNN(9-1-5)
![SRCNN_results](https://github.com/YuanrunXu/USC-EE541-Final-Project-Super-Resolution/assets/43257371/c808212e-183e-4b03-9c86-a9fb2f5902ac)
### SRCNN(5-3-5)

### SRGAN Curves
![SRGAN_results](https://github.com/YuanrunXu/USC-EE541-Final-Project-Super-Resolution/assets/43257371/f1b028ff-62f4-4f1a-8903-30c1bdffc358)


## 3. Folders
The project constains 5 folders.
- data: DIV2K dataset and code of splitting the train dataset into train and validation
- SRCNN: code and model of SRCNN
- SRGAN: code and model of SRGAN
- saved_model: the best trained models
- result: training peremeters tables, training results plots and related images

### data
data folder is the transformation of dataset DIV2K. It contains three subfolders named train, val, and test to store corresponding datasets.  
Original images are in HR and LR folders. Model outputs are in SRCNN folder.  
dataPrepare.ipynb: Split the original train dataset into new train dataset with 550 images and val dataset with 250 images. Rename the original valid dataset as new test dataset.

### SRCNN
- SRCNN_training_2.0.ipynb: the main code to train and evaluate the SRCNN
- SRCNN_data_loading.py: load train, validation, and test dataset from the Data folder
- SRCNN_image_show.py: class to plot the output images
- SRCNN_logger.py: class to record training criterions (Loss, SNR, PSNR, SSIM) and plot
- SRCNN1.py: define the model class SRCNN(9-1-5)
- SRCNN2.py: define the model class SRCNN(5-3-5)

### SRGAN
- SRGAN_training_1.0.ipynb: the main code to train and evaluate the SRGAN
- SRGAN_data_loading.py: load train, validation, and test dataset from the Data folder
- SRGAN_image_show.py: class to plot the output images
- SRGAN_logger.py: class to record training criterions (Loss, SNR, PSNR, SSIM) and plot
- SRGAN.py: define the model class SRGAN

### saved_model
- best_model_915: the peremeters of the best SRCNN(9-1-5)
- best_model_915: the peremeters of the best SRCNN(5-3-5)
- best_SRGAN_generator: SRCNN(9-1-5)


## 4. Deployment
* Put the DIV2K dataset into the Data folder, then run dataPrepare.ipynb  
* SRCNN & SRGAN Training: run the corresponding code of .ipynb. The model peremeters will be automatically saved in saved_model folder for test evaluation in the code. If the folder does not exist, the code will create first.  
* The code could use .csv files to plot the model performance and save it as .png files.


