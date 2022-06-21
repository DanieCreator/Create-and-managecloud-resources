# A project in the Professional Data Engineer certification path
##
##
##CREATING A VIRTUAL MACHINE
--Task 1. Create a new instance from the Cloud Console
--In the Cloud Console, on the Navigation menu (Navigation menu icon), click Compute Engine > VM Instances.
--To create a new instance, click CREATE INSTANCE.
--There are many parameters you can configure when creating a new instance. Use the following for this lab:
***instance name
***Region
***zone
***Machine Series
***Machine type
*** Boot Disk
***Firewall
--Click Create.
--To use SSH to connect to the virtual machine, in the row for your machine, click SSH.
##Task 2. Install an NGINX web server
--In the SSH terminal, to get root access, run the following command:
         --sudo su -
--As the root user, update your OS:
         --apt-get update
--Install NGINX:
          --apt-get install nginx -y
--Confirm that NGINX is running:
          --ps auwx | grep nginx
          
--To see the web page, return to the Cloud Console and click the External IP link in the row for your machine, or add the External IP value to http://EXTERNAL_IP/ in a new browser window or tab.

##Task 3. Create a new instance with gcloud
--In the Cloud Shell, use gcloud to create a new virtual machine instance from the command line:
   --gcloud compute instances create gcelab2 --machine-type n1-standard-2 --zone us-central1-f
   
--In the Cloud Console, on the Navigation menu, click Compute Engine > VM instances. Your 2 new instances should be listed.
--You can also use SSH to connect to your instance via gcloud. Make sure to add your zone, or omit the --zone flag if you've set the option globally:
       --gcloud compute ssh gcelab2 --zone us-central1-f
