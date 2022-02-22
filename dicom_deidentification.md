# Download Workflows from BioDepot-LLC Repository

- Use the Git command to clone the repository https://github.com/Biodepot-LLC/workflows
- Download the compressed file and then unzip the workflows.

On the menu bar, select **File** then **Load workflow**

![](./gatk_workflow/gatk_workflow_load_workflow.png)

Select the workflow in directory **workflows/general/DICOM_Deidentification**

![](./dicom_deidentification/dd_load.png)

There are three widgets in DICOM De-identification workflow

![](./dicom_deidentification/dd_workflow.png)

- **DICOM Uploader**: to upload DICOM images
	+ Credential File: the credential file that is generated from Google Cloud Platform (GCP) console. https://console.cloud.google.com/apis/credentials
	+ DICOM Directory: the directory includes DICOM images
	+ Bucket Name: the Google Storage bucket name that already created. https://console.cloud.google.com/storage/browser
	+ Project ID: the project ID associate with the GCP billing account. https://console.cloud.google.com/projectcreate
	+ Location: the location of the service. (default is us-central1)
	+ Dataset: the dataset. https://console.cloud.google.com/healthcare/browser
	+ DICOM Store: the DICOM store in a dataset.
- **Google Healthcare API (Deidentification)**: to specify the fields in DICOM images and execute the process of Deidentification through the API
	+ Credential File: the credential file that is generated from Google Cloud Platform (GCP) console. https://console.cloud.google.com/apis/credentials
	+ Project ID: the project ID associate with the GCP billing account. https://console.cloud.google.com/projectcreate
	+ Location: the location of the service. (default is us-central1)
	+ Dataset: the dataset. https://console.cloud.google.com/healthcare/browser
	+ Deidentified Dataset: specify name of the output deidentified dataset.
- **Slim & OHIF viewers**: to execute the Workflow Description Language (WDL) script
	+ Credential File: the credential file that is generated from Google Cloud Platform (GCP) console. https://console.cloud.google.com/apis/credentials
	+ Project ID: the project ID associate with the GCP billing account. https://console.cloud.google.com/projectcreate
	+ Location: the location of the service. (default is us-central1)
	+ Dataset: the dataset. https://console.cloud.google.com/healthcare/browser
	+ DICOM Store: the DICOM store in a dataset.
	+ Client ID: the authorized client application. https://github.com/varikmp/dicom_viewers/tree/documentation#setting-up-google-cloud

### Tutorials

1\. From the DICOM uploader widget, we need to select the credential file to allow the widget to operate the uploading. The DICOM directory should include the DICOM images and there is no particular level of sub-directories it holds. The Google Storage bucket name need to be specified to upload images to (They will be all deleted after transferring to the DICOM Store in the Dataset). Project ID, Location, Dataset, and DICOM Store are all information that we need to fill in for the purpose of this widget.

![](./dicom_deidentification/dd_du.png)

2\. The workflow directly transfer to Google Healthcare API widget after the previous one complete. Before putting this widget in progress, there will be a window popped up to ask user selects what DICOM fields the prefer to remove out of the metadata and images.

![](./dicom_deidentification/dd_gha_fields.png)

3\. We can also save the same DICOM field configuration to use for the next time by select the file in **optional entries** tab.

![](./dicom_deidentification/dd_gha_file_saved.png)

3\. The widget will automatically configure the settings and process the deidentification, and the screen should be similar as the picture shown below.

![](./dicom_deidentification/dd_gha_complete.png)

4\. The workflow again transfer to the last widget to display the uploaded and deidentified DICOM images over the viewers SliM (Slide Microscope) and OHIF (Open Health Imaging Foundation).

![](./dicom_deidentification/dd_sov_login.png)

5\. After logging in successfully, we should be able to view the DICOM images with two options (2 tabs) SliM and OHIF as below.

Note: make sure that we already had the client app authorized by GCP before this step. https://github.com/varikmp/dicom_viewers/tree/documentation#setting-up-google-cloud

![](./dicom_deidentification/dd_sov_ohif.png)

![](./dicom_deidentification/dd_sov_slim.png)

![](./dicom_deidentification/dd_sov_slim_d.png)

### Tutorial Video:

<a href="https://www.youtube.com/watch?v=KNEh_kGAl44&ab_channel=VarikHoang"><img src="./dicom_deidentification/biodepot_gh_api.bmp" width="50%" height="50%"></a>
