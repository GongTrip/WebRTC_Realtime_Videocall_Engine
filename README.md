# WebRTC_Realtime_Videocall_Engine
WebRTC enables real-time peer-to-peer video communication. 
Running WebRTC locally requires Google App Engine SDK for Python. 
If using Google Cloud Engine VM's for Collider, Change `WSS_INSTANCE_HOST_KEY`, `WSS_INSTANCE_NAME_KEY` and `WSS_INSTANCE_ZONE_KEY` to corresponding values for your VM instances which can be found in the Google Cloud Engine management console.  
Else if using other VM hosting solution, Change `WSS_INSTANCE_HOST_KEY` to the hostname and port Collider is listening too, e.g. localhost:8089 or otherHost:443.  

REMEMBER: 

> Enabling Local Logging; Note that logging is automatically enabled when running on Google App Engine using an implicit service account. By default, logging to a BigQuery from the development server is disabled. Log information is presented on the console. Unless you are modifying the analytics API you will not need to enable remote logging. Logging to BigQuery when running LOCALLY requires a `secrets.json` containing Service Account credentials to a Google Developer project where BigQuery is enabled.  

> DO NOT COMMIT `secrets.json` TO THE REPOSITORY.  

To generate a `secrets.json` file in the Google Developers Console for your project:  

1. Go to the project page. 

2. Under *APIs &amp; auth* select *Credentials*. 

3. Confirm a *Service Account* already exists or create it by selecting *Create new Client ID*. 

4. Select *Generate new JSON key* from the *Service Account* area to create and download JSON credentials. 

5. Rename the downloaded file to `secrets.json` and place in the directory containing `analytics.py`.
