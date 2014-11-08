#### MODIFY PDF TO EXECUTE EXE IN WINDOWS WITH PARAMETERS
1. Open the modified version of the “launch.pdf” PDF file from the previous exercise with your favorite text editor and revisit the object number 108.
2. Modify the /F Byte string to (notepad.exe) to specify we are going to execute notepad from within the PDF file. To pass parameters we need to add the /P name object parameter followed by a string containing the parameters. Modify the launch.pdf file object number 108 to look like the following excerpt to pass a file name of test.txt to notepad:

  ```
  <<
  /F (notepad.exe) /P (test.txt)
  >>
  ```

3. Save your changes and reopen the “launch.pdf” file in Adobe Reader to verify that notepad is executed and you are prompted to create a new file called “test.txt”. As you can see passing parameters to any application is easy with the /P name object parameter. In future PDF related learning modules we will look at performing attacks using this name object parameter to pass “cmd.exe” interesting scripts and strings to perform actions for us.
4. This concludes the lab exercise, continue to exercise 3.
 
