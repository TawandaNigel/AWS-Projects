<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Tawanda Nigel Chitapi  
**Email:** nigel.chitapi@gmail.com

---

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to use S3 to host a static website. I am doing this project to learn about AWS and cloud services and how they can be used to store objects in the cloud AND even host websites (how does that work?!)

### Tools and concepts

Services I used were Amazon S3. Key concepts I learnt include Bucket Policies, uploading static website files, index.html, bucket endpoint URLs and ACLs and how the control access to bucket objects

### Time, challenges, and wins

This project took me approximately 1hr 30 mins, including demo time, quiz time and secrect mission time. This is definetely archivable in less than 15 mins.  The most challenging part was resovlving the 403 Forbidden error.  It was most rewarding to see the webpage load and be live and public to the world.

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will create an S3 bucket, because i need to create a storage space for the website files.

### How long it took to create the bucket

Creating an S3 bucket took me less than 5 minutes. I had to go over ACL and Bucket Versioning concepts.


### Region selection

The Region I picked for my S3 bucket was Oregen because it is the region that is closest to me. It is best practise to pick the region close to you because it reduces latency and costs, although this is not important for this project.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means no two AWS S3 buckets in the entire world can have the same name. they have to be completely unique 

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will upload the website files into my S3 bucket. This is important because without any files there is no website to host. 

### Files I uploaded

I uploaded two files to my S3 bucket - they were an index.html file. this determine the structure (i.e what goes into your websites) and a folder with images that will go onto the website itself.

### How the files work together

Both files are necessary for this project as index.html determines the structure but the structure alone does not illustrates the contents of the website. (i.e if index.html say insert image here,) you might not have the image to show and so you need to supply the images and various other assets that the website needs to display. 

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will make the website available to the world. This is called Static Website Hosting. This is important because our website files will stay as just files and not turn into websites if I do not do this step. 

### Understanding website hosting

Website hosting means putting our websites files onto a web server, which is a computer designed to turn the files into a website page that people can visit.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I went into the properties tab of my bucket and enables static website hosting and I also labelled the the index.html as the file that i would like to host 

### Access Control Lists (ACLs)

An ACL is a way to configure permission settings in a bucket. I enabled ACLs so that i can control access to the website files later. There was a pop-up mentioning that AWS recommends disabling ACLs but we will keep it enabled to learn abot ACLs and compare them with bucket policies later.

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is a url that takes you to the website that you are hosting.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw an error. 403 forbbiden error. The reason for this error was because objects in a bucket are private by default even though I switched off block all public access. the website files themselves are stilled locked. I need to made their public access permissions so that they are visible to the public. 

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will go into the files that i uploaded into my bucket and make them public, because this will enable the content of the website to be visible. 

### How I resolved the 403 error

To resolve this 403 Forbidden error, I navigated to the objects panel on my S3 bucket and check off both the index.html file and the assets folder and then selected actions and chose make public using ACLs. This then made the files publicly accessible to the world. 

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about to use Bucket Policies to control access to the bucket files. I'm doing this so that we can stop people from deleting the objects with the buckets.

### Understanding bucket policies

An alternative to ACLs are bucket policies, which are rules that determine who is allowed or not allowed to do something. The benefit of using bucket policies is that you can have even greater control of accesss of the actions that people can or cannot make, while ACLs are useful for controlling public access to individual objects within the bucket.

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policy denies everyone from deleting the index.html file in the bucket. I tested this by attempting to delete index.html and saw an access denied error, meaning the bucket policy worked effectively. It stopped me from deleting the object i intended to protect.

---

---
