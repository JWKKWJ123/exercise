# exercise
Create a csv/excel file which include the information needed for the uploading of each scan   
Only **scan path and scan label** are needed beforehand, because these can be dataset specific, other information can all be extract based on **scan path**. 

# Hello World


# Xnat_upload_general.py

- project: string of XNAT project ID
- subject: string of XNAT subject ID (called PTID in the csv file)
- scan_type: string indicating scan type (e.g. T1 or FLAIR)
- scan_path path to scan on local computer
- scan_label: string of label, e.g. 001_S_0001_bl, can also be called experiment label, the scans in the same experiment have the same label
- scan_id: string of scan id that is provided during XNAT upload
- scan_date: The time the scan was created
- scan_discription: string of discription of the scan, exract from DICOM head file
- scan_notes: string of notes relate to the scan, it can be anything


# Hello World



# run.sh
bash file used to submit job to the GPU-cluster.   
information needed in the bash file 
- host: Xnat host (e.g. BIGR Xnat 'https://bigr-rad-xnat.erasmusmc.nl/') 
- user: user name
-password
- project: project name






### vCorrespondence between the information in the csv file and interface of Xnat webpage after uploading
![avatar](https://github.com/JWKKWJ123/exercise/blob/main/Capture.PNG))
