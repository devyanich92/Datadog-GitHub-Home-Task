# Datadog-GitHub-Home-Task
The Challenge for -- Support engineer role

I really enjoyed speaking to Alex the other week and apologise for the late submission. After that conversation, I went on holiday for two weeks to see family and friends in India.

While in India, I read through the references provided and established a background on what the task is and how the Datadog software works.

Here is my submission, I hope I’ve covered all the points well, I would love to work for a company like Datadog.

## Level 0 – Installing Vagrant and VirtualBox
 
I followed the steps mentioned in the links provided in “Guide to the agent” to download and install Vagrant and VirtualBox.

I initially tried to manually run the package that I had downloaded from the web for Vagrant, only realising it after that I should probably try having the pre-requisite “VirtualBox”.

After installing both VirtualBox and Vagrant and running the commands in terminal I had the system up and running!

<img width="1276" alt="1" src="https://cloud.githubusercontent.com/assets/28378176/26140373/b7fe79c4-3b19-11e7-842d-d5e86755d4ba.png">

<img width="835" alt="2" src="https://cloud.githubusercontent.com/assets/28378176/26140535/c67318d8-3b1a-11e7-8032-fe711f76cabb.png">

It took a lot of trial-and-error to get the VirtualBox correctly working.

A few errors that I encountered on my way to get Vagrant and VirtualBox working are shown as below:

<img width="1280" alt="3" src="https://cloud.githubusercontent.com/assets/28378176/26140597/0b7b9da6-3b1b-11e7-8e51-59b05abe61e2.png">

I overcame these errors by reading various threads and posts on GitHub, I saw a number of posts related to the basic errors that I was getting. I also referred to the reading references provided in the challenge. After watching a couple of videos I realised that I was trying to progress in the wrong direction, and hence I took a break and started with a fresh perspective towards the task.

## Level 1 – Collecting Data

I started this section by downloading the Datadog-Agent via provided link 'https://app.datadoghq.com/account/ settings#agent/ mac'.

Followed the instructions for Agent-installation for Mac OS X as shown below.

<img width="1266" alt="4" src="https://cloud.githubusercontent.com/assets/28378176/26140627/28a75640-3b1b-11e7-9175-e62b35ea942d.png">

<img width="834" alt="5" src="https://cloud.githubusercontent.com/assets/28378176/26140653/555569d4-3b1b-11e7-8c3b-e8c775f5b161.png">

After copy pasting the above mentioned code in my terminal and getting numerous “API key invalid” messages, I got curious and decided to change the API key manually as instructed.

<img width="1000" alt="6" src="https://cloud.githubusercontent.com/assets/28378176/26140797/1ba7ba88-3b1c-11e7-8642-f34a3d5a9167.png">

This worked well, and I finally had the DD-agent up and running!

<img width="1276" alt="7" src="https://cloud.githubusercontent.com/assets/28378176/26140820/3b48330e-3b1c-11e7-859d-abe4a0025304.png">

What is the Agent?

An agent is the software responsible for collecting and delivering the Metrics and Events from the machine (it’s installed on) to Datadog. An Agent has: the collector, dogstatd, and the forwarder as shown below:

<img width="780" alt="8" src="https://cloud.githubusercontent.com/assets/28378176/26140848/588b702a-3b1c-11e7-9eb1-b688d9187d65.png">

<img width="904" alt="9" src="https://cloud.githubusercontent.com/assets/28378176/26140849/58fbbd30-3b1c-11e7-85f8-471f1d6cc17c.png">

Adding Tags in the Agent-Configuration File:

For adding tags in the Agent config file, I read through the references provided and discovered the “Guide to Tagging” documentation.

<img width="807" alt="10" src="https://cloud.githubusercontent.com/assets/28378176/26140992/f29768e0-3b1c-11e7-9192-880640f04072.png">

Browsing through – I found “Adding tags using the Configuration File”. However, every time I clicked on adding tags it would direct me back to the installation step.

Changing my course of thinking: I decided to read through more references and find out more about Adding tags via config files.

One of the references suggested to install the database before adding Tags, it did make sense to me and hence I thought I’d give it a go.

I downloaded MongoDB – simply googled “mongoDB install Mac” and got the link to their official website. After the download I realised that I did have Homebrew package already installed but on running “brew update” it would just give me the error message stating “command not found”.

I tried installing the Xcode from Appstore, and then tried manually running the Xcode for installation.

<img width="727" alt="11" src="https://cloud.githubusercontent.com/assets/28378176/26140988/f1e9e986-3b1c-11e7-862e-3805542d2361.png">

After several failed attempts to install Xcode/homebrew and mongoDB, I decided to give it a shot manually, and IT WORKED!

<img width="877" alt="12" src="https://cloud.githubusercontent.com/assets/28378176/26140984/f19970c8-3b1c-11e7-8a0d-a36aa1283cf1.png">

While doing the manual installation I also decided to change the user from “Datadog” to “Devyani” – for a little personal touch.

<img width="632" alt="13" src="https://cloud.githubusercontent.com/assets/28378176/26140987/f1e8ae18-3b1c-11e7-92a4-ac61217391f3.png">

Further following the instructions, I went onto the Integrations Tab on Datadog-web app and installed MongoDB begin configuration for the same. This is where I changed the User and followed the steps to configure the MongoDB Integration with Datadog-agent.

<img width="1172" alt="14" src="https://cloud.githubusercontent.com/assets/28378176/26140985/f1e78b82-3b1c-11e7-8c0e-dd1793eb6b8d.png">

<img width="900" alt="15" src="https://cloud.githubusercontent.com/assets/28378176/26140986/f1e7b490-3b1c-11e7-9453-69fc63370a85.png">

I did realize while doing the manual configuration – that since I had changed the “user” from “Datadog” to “Devyani” I will have to change it in the Mongo.yaml file as well.

<img width="784" alt="16" src="https://cloud.githubusercontent.com/assets/28378176/26141266/48646830-3b1e-11e7-8615-f8cb08a89460.png">

This is where I found out how to Add tags via Config file. I added area and database tags for testing and hopefully it is correct.

<img width="1272" alt="17" src="https://cloud.githubusercontent.com/assets/28378176/26141260/481a246e-3b1e-11e7-8a46-126e0fcbdd1e.png">

Once I got it working and installed properly I ran ‘Datadog-agent info’ to verify mongo was up and running. 

However, instance #0 was not running properly due to the local host either being incorrect or due to me not having permission rights to access the local host of 27016 (found a couple of references on Datadog—GitHub stating that one instance running would be sufficient for the time being.)

<img width="981" alt="18" src="https://cloud.githubusercontent.com/assets/28378176/26141263/481b65a4-3b1e-11e7-84ff-503da8503326.png">

Write a Custom -- AgentCheck

Read the provided reference –thoroughly “Writing an Agent Check”.

I found the code “your first check” and renamed it to “test.support.random” and formed 2 files with the extensions .py and .yaml.

The location of the .py and .yaml file that I created is shown below. I did edit the code in .py file. Added an ‘import random’ line as the first line of code. Changed the ‘class HelloCheck’ to ‘class RandomCheck’ and edited ‘hello.world’ to ‘test.support.random’.

I had also kept the value for self.gauge as 1, but then later changed it to random.random() to import a random metric rather than with a constant value.

I did not edit the .yaml file.

<img width="710" alt="19" src="https://cloud.githubusercontent.com/assets/28378176/26141261/481aa33a-3b1e-11e7-9532-5c64fdf58d31.png">
<img width="659" alt="20" src="https://cloud.githubusercontent.com/assets/28378176/26141265/481f084e-3b1e-11e7-9c98-04bf86422425.png">
<img width="1263" alt="21" src="https://cloud.githubusercontent.com/assets/28378176/26141264/481bb5cc-3b1e-11e7-931b-6dfd137fb231.png">

Level 2: Visualizing the Data

For visualising the data – I selected ‘Dashboards’ and then ‘Dashboard List’ in the drop down menu. Found the ‘Integration Dashboards’ list and selected the proper integration dashboard (MongoDB here) shown below.

<img width="1275" alt="22" src="https://cloud.githubusercontent.com/assets/28378176/26141262/481b1cde-3b1e-11e7-85df-a22acdf475d4.png">

Found the settings button in the upper right hand corner of the integration dashboard, and selected ‘Clone Dashboard’ (shown below). Named the dashboard ‘Clone-Mongo’.

This is where I selected Edit Dashboard, and added the metric – test.support.random to report at the dashboard.


