# Lab Report 5: VIM Command Line Task 
This lab report will provide a chronological step-by-step procedure on how to fork and clone a repository and utilize VIM to help edit/modify/save the file. 

**Objectives:**
- [ ] Clone your fork of the repository from your Github account  
- [ ] Open and edit the file directly in the terminal  
- [ ] Debug the code to have tests run successfully 
- [ ] Commit and push the resulting change to your GitHub account 


## Step 1: SetUp: Delete Existing Repository 
You may or may not have already forked this file so let's start over for this assignment by deleting. 
1. Log into your GitHub account and on the top right corner, click on your profile and click on `your repositories` <br /> <img src="step1_1.png" width="250" height="220"/>
2. Click onto the repository that you are trying to work with and go to its 'settings` on the far right at the top <br /> <img src="step1_2.png" width="800" height="70"/>
3. Scroll onto the bottom and choose the option to `delete this repository`.  <br /> <img src="step1_3.png" width="700" height="400"/>
4. Open your terminal on the computer and log into your @ieng6 account. Note: My login did not prompt for password input as I already had set up the SSH Key to my account. If you have not set up the SSH key, then your terminal should still ask if "you want to continue connecting" and be prompted for a password input. <br /> <img src="step1_4.png" width="500" height="200"/>
5. In the terminal, remove the directory from your account by using the command `rm -r lab7/`. You can log out afterwards once you finished this step. Notice that when you use `$ ls` afterwards, lab7 is no longer in the content. You should be able to see a similar result in your terminal like the picture below. <br /> <img src="Step1_5.png" width="800" height="90"/> 

## Step 2: Fork the Repository 
Click on the [link](https://github.com/ucsd-cse15l-s23/lab7) to fork Lab 7's repository by going to the top right corner. <br /> <img src="step2.png" width="500" height="160"/>

## Step 3: Begin The Timer
Set a timer before you start doing the tasks of logging into your specific account, cloning the repository, and editing the file. 

## Step 4: Log Into Your Account Using ieng6
In the terminal, login into your account using `$ ssh cs15lsp23zz@ieng6.ucsd.edu`. This step is similar part 5 of step 4. Refer to the picture from that step if needed to clarify the result display. 

## Step 5: Clone Your Repository That You Forked 
1. In the terminal, git clone the repository that you have done in your GitHub account into the ieng6 account. You can simply go to the forked repository in GitHub on a new tab and copy the link from the browser to complete the following command in your terminal. `$ git clone <the link>` <br /> <img src="step5_1.png" width="600" height="130"/> 
2. After you have cloned into the account, use `ls` to make sure it is successfully cloned. Lab7 should be displayed. <br /> <img src="step5_2.png" width="600" height="50"/> 
3. Change your directory to go into lab7's file using `$ cd lab7/`
4. After you change the directory, you can see the files inside lab7 and check what are the names of the files to pull up to edit later. Use ls to see the contents and your terminal should be similar to the picture shown below. <br /> <img src="step5_4.png" width="600" height="100"/>

## Step 6: Run the Tests to Demonstrate That They Fail
Run the test using the command `$ bash test.sh`
The result in the terminal should be similar to the picture shown below, indicating there are test(s) that have failed. <br /> <img src="step6.png" width="680" height="300"/> <br />
Explanation: The command will run the tests using JUnit for the ListExamples.java file. Run indicates how many the tests passed and failures indicates the amount of tests have failed. Read the description of the output to see possible errors. 

## Step 7: Fix the Code So Test Can Run 
1. In the terminal, use the command `$ vim ListExamples.java` and press `<enter>` so the contents of the file will be opened. Your terminal should display like similar to the picture below. <br /> <img src="step7_1.png" width="600" height="750"/> 
2. Follow the instructions to modify the code. 
#### First Step: Move Your Cursor Until It Reaches the Correct Line 
We need to modify the code where it is commented to "change index1 below to index2 to fix test". <br /> <img src="step7_2_1.png" width="400" height="55"/> <br />
You can either 
* Option 1: Press key `J` (helps you move the cursor downwards) until you reach the code line OR 
* Option 2: Use the command `/<toFind>` where toFind is the specific keyword you are looking for to see if it exists in the code. In this case, you can use `/index1`

#### Second Step: Move the Cursor Until It is One Space After Number "1" 
Once you have reached the right line of code to edit, use the key `L` on your keyboard to move your cursor to the right until it is exactly one space after "1" of the variable index1. <br />
<img src="step7_22.png" width="400" height="55"/> <br />

#### Third Step: Change "1" to Become "2"
* Part 1: Press on the key `i` on your keyboard so that you can be changed into Insertion Mode within the file and make modifications. At the bottom of your terminal, you should see "insert" like the picture below. <br />
<img src="step7_3_1.png" width="400" height="120"/> <br />
* Part 2: Press `<delete>` to remove "1" from variable "index1" 
* Part 3: Press the number `2` on your keyboard to make it become "index2" 
* Part 4: Press `<escape>` to exit from Insertion Mode 

After this step, you should have changed part of your code. <br />
Before: <br /> <img src="before.png" width="400" height="60"/>  <br />
After:  <br /> <img src="after.png" width="400" height="60"/>  <br />

***Note: DO NOT do anything after this step and follow onto the next step.***
### Step 8: Run the Tests to Demonstrate That They Pass
1. After you have finished editing, make sure to save the modified file. Use the command `:wq` and press `<enter>` to save the edited file. <br /> <img src="step8_1.png" width="250" height="170"/>  
2. Then press `<return>` and press `<enter>` to exit the file to bring the user back to the terminal command's line. 
3. Once you reach this step, you have already fixed the error. Let's run the tests now to see if they all will pass or fail. Just like how you ran the tests previously from step 6, type the command `bash test.sh` once more in the terminal. Your terminal should display the result similar to the picture being shown below. <br /> <img src="step8_3.png" width="680" height="340"/>

### Step 9: Commit and Push Your Edited Contents to GitHub 
1. Add the modified file/content into the repository. In the terminal, type in the command `$ git add ListExamples.java` and press `<enter>`
2. Then, commit the modified file with a newly updated message. In the terminal, type in the command `$ git commit -m "<yourChosenMessage"`. Within the quotation marks, you have the choice of writing any commit message of your choice as it is your own work so put something to let yourself know the file has been changed. An example in the correct format with the message "index1 was updated" is: `$ git commit -m "index1 was updated"`. Press `<enter>` after to see the following result similar to your terminal's display. <br /> <img src="step9_2.png" width="600" height="440"/>
3. Lastly, we want to push our modified contents into the forked repository. In the terminal, type in `$ git push origin` and press `<enter>`. You should see a similar result in your terminal like the picture shown below. <br /> <img src="push_success.png" width="600" height="440"/>
4. ***SKIP THIS STEP IF YOU SUCCEEDED PREVIOUS PART OF STEP 9***: For those who have failed to push their files from the previous step, let's resolve the problem. Did the terminal ask you for your GitHub account's username and then prompted for your password? Did you try putting your GitHub account's password once or maybe many times and it results in "authentification failed..."? The reason is because if you have enabled two factor authentification associated with the account you signed up for, this also means you need a second factor for when you try to acess GitHub. In order for you to do this, you need to create a personal access token, one where you can use as a password for you to have access to your work. Follow the steps below: 
   * 1) Click on this [link](https://github.com/settings/tokens). You will see this webpage. <br /> <img src="go_intoken.png" width="600" height="440"/>
   * 2) Click on "Generate new token" tab and select either choice. If you are not sure, please read the [documentation](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) before selecting <br /> <img src="token_choose.png" width="600" height="440"/>
   * 3) You will then either have one of the two displays after choosing
     - Fine-grained, repo-scoped: 
     <br /> <img src="grained.png" width="600" height="440"/>
     - General use (classic): 
     <br /> <img src="classic.png" width="600" height="440"/>
   * 4) Fill out the required information to create your token and scroll down at the bottom of the page and click on `generate new token` 
   * 5) Your webpage will then display something similar below with your access token key. ***NOTE:*** Make sure you save this key somewhere if you will encounter login authentifications with GitHub within the time frame the key is not expired yet as it will disappear after you exit the browser. <br /> <img src="token_created.png" width="600" height="440"/>
   * 6) Copy the special token and go back into the terminal to paste it into the prompted password for git push origin and you should be able to see the successful git push from the picture in the previous instruction of step 9.  

### Conclusion: 
Great job following the instructions! We were able to: 
- [x] Clone your fork of the repository from your Github account  
- [x] Open and edit the file directly in the terminal  
- [x] Debug the code to have tests run successfully 
- [x] Commit and push the resulting change to your GitHub account 
Now you can try editing other programming assignments that you have forked from GitHub wth these steps that you have learned! 

***NOTICE:*** You may or may not have completed all these steps due to complications in typing in certain commands. Note that the `$` in the code block is to indicate the starting point of where you should start typing in the command, so DO NOT include `$` in your commands. Check for typos for possible extra <space> or incorrectly spelled commands. Otherwise, you can copy and paste the commands from these instructions for the appropriate steps and fix certain parts accordingly such as the ssh command to your ieng6 account to match your id or certain messages that you want to search or commit. 
