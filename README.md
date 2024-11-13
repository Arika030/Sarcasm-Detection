# Sarcasm-Detection

Once logged in the breakdown of the google drive is as followed:
- Training: Folder of the Reddit dataset, contains the modified and the original dataset along with a README detailing the modifications: https://drive.google.com/drive/folders/1FJ08W-KytoyNFP1GevN9PybRWqzAQDHc?usp=drive_link
- Testing: Folder which holds the Sarcasm Corpus & Twitter data we used for the external data testing: https://drive.google.com/drive/folders/1tn0RzsZhU78Epb5SP-9asOmzDK3X87R-?usp=drive_link
- t5_base_reddit_sarcasm: Folder which holds the finished fine-tuned model. The model currently in the folder is fine tuned on the Reddit dataset. https://drive.google.com/drive/folders/1SIDVsFVP_zjiCRRof54iAU6g3h4_iQMc?usp=drive_link
- Sarcasm_twitter_test_output: Folder which contains metrics and visual of the statements the model attempted to predict: https://drive.google.com/drive/folders/1-4YDQU8PvomkT0D8_PZSISStEwphdFrN?usp=drive_link
- Sarcasm_corpus_v2_test_output: Folder which contains metrics and visual of the statements the model attempted to predict: https://drive.google.com/drive/folders/1ktD3EHEFgB7tWWVOUIHoUWhX5OEGfLl0?usp=drive_link
- old fine tuned models: folder that is empty, meant to hold older versions of the t5_base_reddit_sarcasm folder contents https://drive.google.com/drive/folders/1j5lDZXTMdlN6BWsfpt-1uDWrUN6OrHcJ?usp=drive_link

HOW TO RUN:
- RUN the cells in sequential order. The 1st cell will create a prompt attempting to connect to the google drive. Click Accept for all prompts and the notebook will connect to the google drive. 
- When executing the trainer.fit(model) cell, this will fine tune the model for the given max epochs. The next cell (save_pretrained) will save the model with the best 'val_loss' to the google drive under the folder named: 't5_base_reddit_sarcasm'.
-   ******IMPORTANT: if you are going to fine tune another model, move the entire 't5_base_reddit_sarcasm' folder to the 'old fine tuned models' folder to save the previous work. The 'save_pretrained' command will overwrite whatever is in the folder otherwise.
-   The external testing data will be referenced and the model in the t5_base_reddit_sarcasm folder will be used when executing the post fine tune model testing section.
