# Lab Report 5: VIM Command Line Task 
This lab report will provide a chronological step-by-step procedure on how to fork and clone a repository and utilize VIM to help edit/modify/save the file. 

## Step 1: SetUp: Delete Existing Repository 
You may or may not have already forked this file so let's start over for this assignment by deleting. 
1. Log into your GitHub account and on the top right corner, click on your profile and click on `your repositories` <br /> <img src="step1_1.png" width="250" height="280"/>
2. Click onto the repository that you are trying to work with and go to its 'settings` on the far right at the top <br /> <img src="step1_2.png" width="800" height="90"/>
3. Scroll onto the bottom and choose the option to `delete this repository`.  <br /> <img src="step1_3.png" width="700" height="450"/>
4. Open your terminal on the computer and log into your @ieng6 account. <br /> <img src="step1_4.png" width="500" height="230"/>
5. In the terminal, remove the directory from your account by using the command `rm -r lab7/`. You can log out afterwards once you finished this step. <br /> <img src="Step1_5.png" width="800" height="100"/> 

## Step 2: Fork the Repository 
Click on the [link](https://github.com/ucsd-cse15l-s23/lab7) to fork Lab 7's repository by going to the top right corner. <br /> <img src="step2.png" width="500" height="200"/>

## Step 3: Begin The Timer
Set a timer before you start doing the tasks of logging into your specific account, cloning the repository, and editing the file. 

## Step 4: Log Into Your Account Using ieng6
In the terminal, login into your account using `$ ssh cs15lsp23zz@ieng6.ucsd.edu`. This step is similar part 5 of step 4. Refer to the picture from that step if needed to clarify the result display. My login did not prompt for password input as I already had set up the SSH Key to my account. 

## Step 5: Clone Your Repository That You Forked 
1. In the terminal, git clone the repository that you have done in your GitHub account into the ieng6 account. You can simply go to the forked repository in GitHub on a new tab and copy the link from the browser to complete the following command in your terminal. `$ git clone <the link>` <br /> <img src="step5_1.png" width="600" height="130"/> 
2. After you have cloned into the account, use `ls` to make sure it is successfully cloned. Lab7 should be displayed. <br /> <img src="step5_2.png" width="600" height="50"/> 
3. Change your directory to go into lab7's file using `cd lab7/`
4. After you change the directory, you can see the files inside lab7 and check what are the names of the files to pull up to edit later. Use ls to see the contents and your terminal should be similar to the picture shown below. <br /> <img src="step5_4.png" width="600" height="100"/>

## Step 6: Run the Tests to Demonstrate That They Fail
Run the test using the command `bash test.sh`
The result in the terminal should be similar to the picture shown below, indicating there are test(s) that have failed. <br /> <img src="step6.png" width="680" height="340"/> <br />
Explanation: The command will run the tests using JUnit for the ListExamples.java file. Run indicates how many the tests passed and failures indicates the amount of tests have failed. Read the description of the output to see possible errors. 

## Step 7: Fix the Code So Test Can Be Successful 


