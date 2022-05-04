# MSc_AI_Thesis
Following steps need to be executed to run the code submitted. 
NOTE: Access to image datasets needs user's Google Drive access and Kaggle API credentials

1. Run code snippet 1 to install all the dependencies

2. Run code snippet 2, 3 for Work package 1 -- hospitalization
	a. Mount your Google Drive
	   	drive.mount('/content/gdrive', force_remount=True)

	b. Save all the images taken from below link in your Google Drive
	   	'https://github.com/ieee8023/covid-chestxray-dataset/tree/master/images'
	
	c. Manually 'Accept' to give permission to Google COLAB to access above images from user's Google Drive
	
3. Run code snippet 4, 5, 6, 7 for Work package 2 -- ICU admission
	a. Get Kaggle API credentials using steps mentioned in below link
	   	'https://medium.com/unpackai/how-to-use-kaggle-datasets-in-google-colab-f9b2e4b5767c'
	
	b. In code snippet 4, use below code with API credentials to download and access the Kaggle data in Google COLAB
	   </
	   	# Get kaggle data
	   	!mkdir ~/.kaggle 
	   	!echo '{"username":<USERNAME>,"key":<KEY>}' > ~/.kaggle/kaggle.json 
	   	!chmod 600 ~/.kaggle/kaggle.json  
	   	!pip install kaggle 

	   	# !kaggle datasets list 
	   	!kaggle datasets download -d anasmohammedtahir/covidqu  
	   	!unzip covidqu.zip
	    />

	c. In code snippet 5, save the V-net model in mounted Google drive as mentioned in below functions and codes respectively	   	
		$$function 'save_model'
		%cp /content/model.json /content/gdrive/My\ <Your Google Drive location>/model.json
  		%cp /content/model.h5 /content/gdrive/My\ <Your Google Drive location>/model.h5

4. Run code snippet 8 for Work package 3 -- Life Support transfers
	a. Get pre-trained V-net weights saved in your Google Drive 
		$$function 'get_saved_model'
		%cp /content/gdrive/My\ <Your Google Drive location>/model.json /content/model.json 
		%cp /content/gdrive/My\ <Your Google Drive location>/model.h5 /content/model.h5 

5. Run code snippet 9 for Work package 5 -- LIME-XAI   
