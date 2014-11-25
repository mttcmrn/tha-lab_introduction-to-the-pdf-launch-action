#### MODIFY PDF TO EXECUTE EXE IN WINDOWS

1. Download the template [PDF file](https://github.com/madsec/tha-lab_introduction-to-the-pdf-launch-action/raw/master/launch.pdf) titled: “launch.pdf”.

2. Open the PDF file “launch.pdf” in Adobe Reader version 9.3.0 to verify that it launches the built in Windows calculator “calc.exe”. Note: Newer versions of Adobe Reader have implemented safe guards against launching arbitrary content, so you will need to install version 9.3.0 per the instructions in the Lab Setup section of this learning module.

3. Open the PDF file “launch.pdf” in your favorite text editor and locate the object number 108. This is where we define what application is executed within the PDF file. Take note of the syntax for this object:

  ```bash
  /Type /Action
  /S /Launch
  /Win
  <<
  /F (calc.exe)
  >>
  ```

4. Modify the /F Byte string to (cmd.exe) and reopen the PDF file with Adobe Reader which should result in the Windows Command Shell being launched.

5. This concludes the lab exercise, continue to exercise 2.
