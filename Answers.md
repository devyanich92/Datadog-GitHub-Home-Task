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

ADD PIC 10 HERE

Browsing through – I found “Adding tags using the Configuration File”. However, every time I clicked on adding tags it would direct me back to the installation step.

Changing my course of thinking: I decided to read through more references and find out more about Adding tags via config files.

One of the references suggested to install the database before adding Tags, it did make sense to me and hence I thought I’d give it a go.

I downloaded MongoDB – simply googled “mongoDB install Mac” and got the link to their official website. After the download I realised that I did have Homebrew package already installed but on running “brew update” it would just give me the error message stating “command not found”.

I tried installing the Xcode from Appstore, and then tried manually running the Xcode for installation.


