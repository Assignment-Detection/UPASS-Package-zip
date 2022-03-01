# UPASS - Upload & Pliagarise Alert SyStem 
# Software & Instructions

## What is UPASS

UPASS monitors the internet daily for matches to your assignment questions. Upon detection of a hit, UPASS sends an email notification. 

UPASS will need to be setup and run on a single computer at your institute, however once setup, it can be used by anyone to submit their assignments to from any computer.

Please note that both a SerpStack account and Google account will be required for UPASS to be setup and run. Both are free, however, you may be required to upgrade your SerpStack account to a subscription plan to have sufficient API requests to run UPASS once several assignments have been submitted.


## Uploading Assignments

To setup an alert for your assignment, you will need to complete the google form containing details of your assignment. You will also need to enter search terms. You should try to make the search terms that you enter unique so that they can potentially return matches to your assignment. These may be parts of your assignment brief that have unique questions, subject names, or multiple sentences or a paragraph.


## Serpstack Subscription Plan Requirements

UPASS uses serpstack to perform the online searching. Serpstack has a free tier subscription level. This free tier may be suitable for an individual assignment but it is likely that a paid plan will be required to run UPASS at your institute. The number of serpstack requests that an assignment uses while it is being monitored in UPASS can be calculated by:

_Number of search terms for assignment * Number of days assignment till assignment end date * Frequency of UPASS run in days (i.e. 1 for daily, 0.5 for every other day)_

Depending on how UPASS is setup for your institute and the nature of the assignments uploaded to it, you can estimate which serpstack subscription plan would be required. The pricing for the serpstack subscriptions can be found here: https://serpstack.com/product. Note that serpstack was chosen for this project, but other searching apis would be suitable to use; however, the software code would need to be adjusted to accommodate a different api.


## Installing UPASS

Please follow these steps to setup UPASS for your institute.

Download the UPASS software package from this repository to the computer that will be setup to run UPASS. 

Download the UPASS Package.zip file and extract it where you like. The extracted folder contains several files and sub-directories (refer to the next section if you would like to know more information about these).

In the extracted folder, first open the UPASS Setup Procedure pdf file and follow the steps within.

Next, run the setup_upass.exe file. This will confirm that the setup has been completed successfully. Should any errors be present, a popup will notify you. Please fix the errors before re-running setup_upasss.exe. If the setup has been completed successfully, a popup will notify you.

Now you can share the UPASS submission form throughout your institute and have course coordinators upload their assignment details to it.

The UPASS checks are performed by executing run_upass.exe. Note that the checks will only occur when this executable is run. As such, if you would like UPASS to monitor for assignment uploads every day, this executable will need to be run daily. If you have a Windows computer, you can use the Task Scheduler to automate this for you - this is a helpful tutorial on how to use the Task Scheduler: https://www.windowscentral.com/how-create-automated-task-using-task-scheduler-windows-10

If you wish to get an overview of the details of the assignments which have been uploaded to UPASS at your institute, you can run the upass_overview.exe file. This will open a window displaying all the assignment details and also notify you of the number of current assignments (those that have not reached their end dates yet) in UPASS and total number of search terms for these.


## Files & Directories
* The bin directory contains backend files and directories used by UPASS

* service-account-credentials is a directory where the Google Cloud Platform Service Account json file is to be put (refer to UPASS Setup Procedure.pdf for details)

* UPASS Setup Procedure.pdf contains the instructions for setting up the UPASS assignment detail submission form and linking it with the UPASS backend

* The details for the gmail account which UPASS will use to send notification emails are to be put in the gmail_username.txt and gmail_password.txt files

* The name of the google sheet linked with the UPASS assignment submission form is to be put in the google_sheet_name.txt file (refer to UPASS Setup Procedure.pdf for details)

* run_upass.exe is to be executed after UPASS has been setup, this file executes the checks of the UPASS system.

* Your serpstack api key is to be put into the serpstack_api_access_key.py file (refer to UPASS Setup Procedure.pdf for details)

* setup_upass.exe is to be executed once after completing the steps in UPASS Setup Procedure.pdf, this executable finalises the setup and confirms that UPASS has been set up correctly.

* upass_overview.exe can be executed to view the details of the assignments that are currently uploaded to UPASS (after it has been setup). It also tells the user the number of current assignments in UPASS and the total number of search terms for these assignments.  

To view any of the code, please refer to this GitHub repository: 
https://github.com/Assignment-Detection/UPASS-Upload-Plagiarise-Alert_SyStem


## Copyright

Copyright © 2021-2022 Edmund Pickering, Sam Cunningham, Sarah Dart and Rick Somers. This software is available for non-commercial use only. Commercial use is prohibited unless permission from the authors is given upon request. Any other usage is prohibited without the express permission of the authors. 
