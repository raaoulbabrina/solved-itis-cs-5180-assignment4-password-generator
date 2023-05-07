Download Link: https://assignmentchef.com/product/solved-itis-cs-5180-assignment4-password-generator
<br>
In this assignment you will get familiar with Android concurrency models. The app is a password generator app to help the user to choose strong passwords. The User selects how many passwords they want the app to generate, the length of each password and then chooses one of them. This application is composed of a single activity, namely the Main Activity.

<table width="610">

 <tbody>

  <tr>

   <td width="143"></td>

   <td rowspan="2" width="11"> </td>

   <td width="143"></td>

   <td rowspan="2" width="13"> </td>

   <td width="143"></td>

   <td rowspan="2" width="13"> </td>

   <td width="143"></td>

  </tr>

  <tr>

   <td width="143"><strong>Select Passwords count : </strong>3</td>

   <td width="143"><strong>Select Passwords count : </strong>3</td>

   <td width="143"><strong>Select Passwords count :           </strong>3</td>

   <td width="143"><strong>Select Passwords count :           </strong>3</td>

  </tr>

 </tbody>

</table>

(a) Main Screen             (b) Progress Dialog           (c) Passwords List            (d) Password selected

<h2>Figure 1, App Main Screen</h2>

<strong>Using Threads and Handlers (70 points) </strong>

The interface should be created to match the user interface (UI) presented in Figure 1. You will be using layout files, and strings.xml to create the user interface. Perform the following tasks:

<ol>

 <li>You are provided with a Util class that contains a static method getPassword(int length). The length is the length of the password to be generated. This method is expected to take long time to execute and returns a random String password. Import the provided Java file by simply dragging the file into the src folder under your project package in Android Studio.</li>

 <li>You should create a thread pool of size 2, and use the pool to execute your created threads.</li>

 <li>There are two SeekBars in this assignment:

  <ol start="10">

   <li>Number of passwords SeekBar, this is used to set the number of passwords to be generated. The SeekBar minimum should be 1 and maximum 10. The TextView beside the seeker should show the selected SeekBar progress whenever the user changes the SeekBar progress (moves the SeekBar).</li>

   <li>Password length, this Seek bar is used to set the password length. The SeekBar minimum should be 8 and maximum 23. The TextView beside the seeker should show the selected SeekBar progress whenever the user changes the SeekBar progress (moves the SeekBar).</li>

  </ol></li>

 <li>Tapping the “Generate Passwords (Thread)” button should start the execution of a background thread and return the list of all passwords (based on the selected count and length) by using the getPassword() method. For example, if the count was set to 5, the getPassword() method will run 5 times in the background thread, and return 5 passwords. The list of these 5 passwords should be returned to the main thread and displayed in the AlertDialog. While the passwords are being generated, display a ProgressBar indicating the progress, see Figure1(b).</li>

 <li>To be able to exchange messages between the child thread and the main thread use the Handler class. Either use messaging or setup a runnable message.</li>

 <li>The ProgressBar should not be cancelable. The ProgressBar should be dismissed after all the getPassword() calls are completed. The list of passwords should be displayed using an alert dialog as shown in Figure 1(c).</li>

 <li>Tapping one of the passwords generated should dismiss the Dialog and display the selected password as shown in Figure 1(d).</li>

</ol>

<strong>Part 2 (30 Points): Using AsyncTask </strong>

This part is similar to Part 1, but you should use AsyncTask to implement the same functionality provided by Part 1. Perform the following tasks:

<ol>

 <li>Tapping the “Generate Passwords (Async Task)” button should start the execution similar to Part 1 but using Async Tasks.</li>

</ol>

<strong>Notes:  </strong>

<ol>

 <li>If you are using API level 26 or higher, the ProgressDialog has been deprecated. In this case use ProgressBar. <a href="https://developer.android.com/reference/android/widget/ProgressBar.html">https://developer.android.com/reference/android/widget/ </a><a href="https://developer.android.com/reference/android/widget/ProgressBar.html">ProgressBar.html</a></li>

</ol>