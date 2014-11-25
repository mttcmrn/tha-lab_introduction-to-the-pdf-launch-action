#### USE ORIGAMI-PDF FRAMEWORK TO CREATE A PDF TO EXECUTE FIREFOX AND VISIT THE HACKER ACADEMY WEBSITE

1. Origami-PDF already has a sample script that we can simply modify to our needs within the directory: `/root/THA/pdf-launch-action/assets/origami-1.0.0-beta1/sources/samples/launch` titled “winparams.rb”. Note this script will not work by default so we will have to make some modifications to get it working again.

2. Make a copy of the “winparams.rb” script and name it “firefox.rb” in this same directory. You can do this using the cp command on Linux:

  ```bash
  cd /root/THA/pdf-launch-action/assets/origami-1.0.0-beta1/sources/samples/launch
  cp winparams.rb firefox.rb
  ```

3. If you attempt to execute the firefox.rb script right now you will receive the following error:

  ```
  uninitialized constant Origami::Action::WindowsApplication (NameError)
  ```

    The CHANGELOG.txt found in the “origami-1.0.0-beta1” base directory states that the authors Renamed 'Action::WindowsApplication' to 'Action::Launch::WindowsLaunchParams' , so we need to update the script to reflect this change.

4. Open the firefox.rb script with your favorite text editor so that we can modify it.

5. Go to line 9 which looks like this:

  ```
  params = Action::WindowsApplication.new
  ```

    and modify it to look like this:

  ```
  params = Action::Launch::WindowsLaunchParams.new
  ```

    This updates the script to use the new naming convention and path as stated in the CHANGELOG.txt file.

6. We also want change the functionality of the script to open Firefox and pass the parameter “www.thehackeracademy.com” to it. To do this we need to edit lines 10-13 of the script which currently look like this:

  ```bash
  params.F = "C:\\\\WINDOWS\\\\system32\\\\notepad.exe" # application or document to launch
  params.D = "C:\\\\WINDOWS\\\\system32" # new current directory
  params.P = "test.txt" # parameter to pass if F is an application
  ```

    Modify the above lines to look like this:

  ```bash
  params.F = "firefox" # application or document to launch
  params.P = "www.thehackeracademy.com" # parameter to pass if F is an application
  ```

    Notice we don’t have to specify the full path to FireFox, as it will be in the user’s PATH and will be located by Windows when the user opens the PDF file. Also note we eliminated the “D” parameter line, as it is not needed for our new script. The last modification is passing the string parameter “www.thehackeracademy.com” to FireFox, which will tell FireFox to open this URL.

7. Save these changes and execute the “firefox.rb” script to generate a “firefox.pdf” file.

8. Examine the resulting “firefox.pdf” file with your favorite text editor to better understand the changes and what will happen when you open the PDF file in a PDF reader that supports the Launch action.

9. Verify that the PDF file we generated works correctly by opening it in Adobe Reader Version 9.3.0.

10. This concludes the lab exercise, continue to exercise 5.