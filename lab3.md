#### CREATE A PDF TO EXECUTE AN APPLICATION USING ORIGAMI-PDF
1. Ensure you have installed Origami-PDF on your Kali VM by following the instructions found in the Lab Setup section of this module.
2. Origami-PDF by default already contains a sample for launching different calculator applications depending upon the OS. We are going to examine this sample to better understand it’s inner workings.
3. Change into the `/root/THA/pdf-launch-action/assets/origami-1.0.0-beta1/sources/samples/launch` directory and open the origami-PDF script “calc.rb” with your favorite text editor. Note that the authors of Origami-PDF have left a bunch of useful comments and explanations for what the script is doing and how it works on each OS. I would definitely recommend reading through these notes and becoming familiar with the syntax. Go ahead and close your text editor and the “calc.rb” script once you're finished looking this script over.
4. Let us execute the “calc.rb” Origami-PDF script to examine the actual PDF file generated from this script. To execute the script simply run either of the following commands:

  ```
  ruby calc.rb
  ```

or

  ```
  ./calc.rb
  ```

5. The “calc.rb” script will create a PDF file titled “calc.pdf”. Open this PDF file and examine object 1, as this is where the launch actions for the different OS types occur. Notice that the authors of the script choose to use the file specification options. These file specification options can be found within the PDF specification under section 7.11.2.3 table 43 for your reference. Once you're comfortable with the actions and syntax of the “calc.pdf” file go ahead and close it.
6. Now verify that this PDF file works by testing it on the different Operating Systems you have available. Note that you may need to modify the path on Linux and Unix systems to reflect the correct path for “xcalc”, as described in the comments of the “calc.rb” script and “calc.pdf” file.
7. Generating PDF files by hand in a text editor can be a real pain and this is why I keep reintroducing the Origami-PDF framework into the lab exercises. I would highly recommend you experiment with this framework, as it will save you a bunch of time in generating custom PDF files to use in your PDF attacks.
8. This concludes the lab exercise, continue to exercise 4.

