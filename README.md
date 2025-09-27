Project For the Week*

You need to store a confidential document in Azure Blob Storage while ensuring it remains inaccessible to the public. However, you must share the document with an external user for 5 minutes without granting them full access to the storage account. 

Show the steps to achieve this using a SAS (Shared Access Signature) URL.
Document these steps in your Blog.


And store confidential documents with a Private(no anonymous access)



Good day to everyone reading my Blog, I am Freddie or you can as well call me Techman, i just started creating blogs on Hashnode, today i will be showing us how to Create an Azure Blob Storage account, upload a document then making sure it is not Publicly access, and in the End granting an external user 5 minutes access to the document using SAS (Shared Access Signature) URL without giving them full access to the storage account.

Step 1.
 Go to your Azure Portal via portal.azure.com and sign in with your credentials. In the search bar, search for storage, then click on Storage Accounts.


Step 2.

Click on Create 


Step 3.

Under the Basics Tab, you will see 'Subscription', which is Azure Subscription 1 for those using the Azure Free Tier account. Scroll to 'Resource Group', create a new resource group by giving it a name, and press OK. If you already have a resource group created before, you can proceed with that.


Step 4.

Under Storage account name, give your storage name a unique name, meaning a name that is unique only to your Azure account, that any other Azure users have never used.

 Then select any region of your choice from the drop-down. For the course of this Study, I will select "South Central US".

Primary Service: From the drop-down, select Azure Blob Storage or Azure Data Lake Storage Gen 2.

Performance: Click on Standard

Redundancy Level: From the drop-down down click on Geo-redundant storage (GRS), then below it check the option for "Make read access to data available in the event of regional unavailability" by checking this box. This means we have switched our redundancy level to "RA-GRS".
 Then click Next.


Step 5.

Under the Advanced Tab, make sure you check Allow Enabling anonymous access on individual containers. in other words, in means we are giving permission to our specific container we created in a cloud environment to be accessible without authentication, which we will still restrict access as we proceed in this Blog.
 Then leave every other remaining option as they originally.



Step 6.

Leave every option in step 6 Unchecked. Proceed to the Next step.



Step 7.

Under Blob Storage, you will scroll to Access tier, click on Hot: "Optimized frequent access to data and everyday usage scenarios. which means the access tier you select for your Blob Storage is hot because the type of data you are saving is the type that will be frequently accessed, and this type of access tier provides low latency and high performance.
Then click Next.




Step 8. 

Under the Networking Tab, scroll to network access and click on Enable Public access from all networks, meaning any IP address or network can access the blob URL.


Step 9.

Then scroll down to Network Routing, Routing Preference, Select Microsoft Network Routing, and click Next 



Step 10.

Under the Data Protection Tab, scroll down and check Enable soft delete for blobs. Under days to retain deleted blobs, you can pick days between 1 to 365 days for the course of this study; we will pick 7 days.


Step 11.

Check on "Enable Soft delete for containers, scroll to Days to retain Container, we will pick 7 days like we did earlier. 
 
Then check Enable soft delete for file shares, scroll to Days to retain deleted file shares, we will pick 7 days as well.
Leave other options unchecked as the default.


Step 12.

Leave Step 12 Options Unchecked as the default and click Next.



Step 13.


Under the Encryption Tab, scroll to Encryption Type and click on Microsoft-managed keys (MMK)

Under Enable Support for customer-managed keys, select Blob and files only.
 Proceed by clicking Next.



Step 14.

Under Tags, leave it as the Default. Proceed by clicking Next.



Step 15.

Review and Create Tab, Scroll down and Click on Create.


Step 16.

Deployment in Progress, Wait until it finishes deploying.



Step 17.

Your Deployment is complete. Click on Go to Resource.


Step 18.

After Clicking on go to resource , on your Lower Left side click on Containers.



Step 19.

Click on the + sign to create a container


Step 20.

Give your container a name. In my case, it would be "livingtech" 
Under the Anonymous access level, click on the drop-down and select Private(No Anonymous Access). This is the part to restrict access to your Blob and until you grant access to a specific temporary access to a user to view your blob.
Then click Create.


Step 21.

Once you have given your container a name, check the box beside the name and double click the name of your container. also if you check the anonymous level of our container it has been set to Private, which means unless permission to read is granted , the SAS URL cannot be access by any user.



Step 22. Once you are Inside your created container, Click on the option to select a file to upload, once you are done selecting the specific blob you want to upload into your container, Click Upload and wait for it to get uploaded.



Step 23.

Once your blob has been uploaded into the container, you will see your blob visible inside the cotainer, in my own case for the course of this study my blob uploaded is "AWS DEVOPS SYLLABUS-1.pdf".


Step 24.

Check the Box beside your Blob name and Double click on your Blob uploaded then navigate to Generate SAS



Step 25.

Under generate SAS, navigate to signing methods and click on Account Key.

Signing Key: Key 1

Stored Access policy: None

Permission: In the drop-down down click Read. meaning we are giving a read-only permission to the blob we uploaded.


Step 25. 

Because we are giving a read permission only to the blob we created and our anonymous level has been set to Private which means nobody can access the blob URL, we have to Grant access to a specific user to be able to view our blob for 5 mins via  SAS (Shared Access Signature) URL  Start date: Feb 8th 2025 2:55:29AM  to Feb 8th 2025 3:00:29 AM 

Scroll down to  Allowed protocols and click on HTTPS only.

Click Generate SAS token URL.


Step 26.

Finally, after generating our Blob SAS URL, we will copy the URL and give it to the specific user we granted Read access to, and they can view the Blob for only 5 minutes. After 5 minutes, the permission expires.

Thank you for reading my Blog.













