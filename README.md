## extract_information.py
Create a csv/excel file which include the information needed for the uploading of each scan. In principle, any folder structure and file naming method is acceptable. If the folder structure of raw dataset is irregular, [DeepDicomSort](https://gitlab.com/radiology/neuro/DeepDicomSort_BrainMri_soenke) can be used to creat the path of each scan.
Only **ScanPath, ScanLabel and ScanFormat** are needed beforehand, because these can be dataset specific, other information can all be extract based on **ScanPath**.   
Now the **ScanFormat** is split into: 'DICOM', 'nii', 'PAR' and 'REC'.   

## overview of scans.xlsx
csv/excel file created by _extract_information.py_

## Xnat_upload_general.py
information needed for the uploading of each scan, it can the extracted automatically from the csv/excel and bash file:   
- project: string of XNAT project ID
- subject: string of XNAT subject ID (called PTID in the csv file)
- scan_type: string indicating scan type (e.g. T1 or FLAIR)
- scan_path: path to scan on local computer
- scan_label: string of label, e.g. 001_S_0001_bl, can also be called experiment label, the scans in the same experiment have the same label
- scan_id: string of scan id that is provided during XNAT upload
- scan_date: The time the scan was created
- scan_description: string of description of the scan, extract from DICOM head file
- scan_notes: string of notes relate to the scan, it can be anything

## run.sh
bash file used to submit job to the GPU-cluster.   
information needed in the bash file 
- host: Xnat host (e.g. BIGR Xnat 'https://bigr-rad-xnat.erasmusmc.nl/') 
- user: user name
- password
- project: project name

### Correspondence between the information in the csv file and interface of Xnat webpage after uploading
![avatar](https://github.com/JWKKWJ123/exercise/blob/main/Capture.PNG))
