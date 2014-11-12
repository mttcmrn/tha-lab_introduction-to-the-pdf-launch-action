Hacker Academy
==============
http://hackeracademy.com

### INTRODUCTION TO THE PDF LAUNCH ACTION

#### Purpose
This lab will introduce you to tools and techniques that can be utilized to create and/or construct PDF Launch actions within a PDF file. The PDF Launch action is a built in feature of the PDF specifications that allows us to execute an application and open or print a document. This introductory learning module will lay the groundwork for future learning modules where we will abuse the Launch action to perform some interesting attacks on our target.

#### Requirements
This lab requires a Windows host or VM as well as the following THA virtual machines
* Kali

#### Lab Credentials

* Kali VM: `root / toor`

#### Setup

1. Boot your THA Kali VM and login.

2. Clone this repo on your Kali VM by opening a terminal and issuing the following command:

    ```bash
    git clone git://github.com/madsec/tha-lab_introduction-to-the-pdf-launch-action /root/THA/pdf-launch-action
    ```

3. Run the following command to isntall Origami-PDF on your Kali VM:

  ```
  tar xzvf /root/THA/pdf-launch-action/assets/origami-last.tar.gz
  ```
    * Note: This will install origami-pdf and create a directory titled “origami-1.0.0-beta1”.

4. Install Adobe Reader 9.3.0 on your Windows System. You can get it from the older versions repository located [here](http://www.oldapps.com/adobe_reader.php?app=825D029BE7FB692DADD92DD8875BDBFB).

#### Useful Resources

* Origami-PDF Home Page: http://esec-lab.sogeti.com/dotclear/index.php?pages/Origami
* Origami-PDF Cheat Sheet: http://code.google.com/p/origami-pdf/downloads/list
* Origami-PDF Google Code Project: http://code.google.com/p/origami-pdf/
* Adobe PDF Specifications: http://www.adobe.com/devnet/acrobat/pdfs/PDF32000_2008.pdf
* Adobe JavaScript API Documentation: http://www.adobe.com/devnet/acrobat/pdfs/js_api_reference.pdf
* OLDApps: oldapps.com can be an extremely useful website for a penetration tester, as they tend to maintain a fairly broad repository for older versions of common applications that you will most likely encounter when performing pen testing. http://www.oldapps.com/

##### Note
* If the Kali VM network connection continually disconnects simply reboot the VM.

#### Start the lab
* Follow the instructions for lab 1 found on your Kali machine at 
  ```
  /root/THA/pdf-launch-action/lab1.md
  ```
