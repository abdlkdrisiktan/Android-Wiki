# Android-Wiki
- [Branch](https://docs.gitlab.com/ee/workflow/workflow.html)
- [GitLab and SSH keys](https://docs.gitlab.com/ee/ssh/)
- [Basic commands](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html)
- [Android Setup](https://developer.android.com/studio/install)
- [Git Basic Commit History](https://git-scm.com/book/id/v2/Git-Basics-Viewing-the-Commit-History)
- [Gradle Project Structure](http://tools.android.com/tech-docs/new-build-system/user-guide#TOC-Project-Structure)
- [How I organize Android project structure](https://medium.com/@rey5137/how-i-organize-android-project-structure-5ed9b849dc30)
- [Package by features, not layers](https://medium.com/@cesarmcferreira/package-by-features-not-layers-2d076df1964d)
- [Best practices in Android development by Futurice developers](https://github.com/futurice/android-best-practices)
- [Code Style for Contributors ](https://source.android.com/source/code-style)
- [Architecture Guidelines](https://github.com/ribot/android-guidelines/blob/master/architecture_guidelines/android_architecture.md)
- [Android MVP Architecture: Sample App](https://github.com/MindorksOpenSource/android-mvp-architecture)
- [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)
- [A successful XML naming convention ](http://jeroenmols.com/blog/2016/03/07/resourcenaming/)
- [Refactoring & Design Patterns](https://refactoring.guru/)
- [Display and control your Android device](https://github.com/Genymobile/scrcpy)
- [Android interview questions](Interview.md)


### How to import project

 + Make sure GitLab account connected

 + Go to your computer's shell and type the following command :

```
git clone {URL_GIT} || {URL_HTTPS}
```

### README file properties
  `README.md`
+ should be created in the project root
+ should be written in English
+ should be written using markdown

### Display logcat via terminal 
+ Open terminal using ```Ctrl + T```
+ Find emulator or devices want to logcat 

```
adb devices
```
+ Note the emulator or devices id
+ Start logcat using this command 
```
adb -s {DEVICE_ID} logcat
```

### How to create new branch
+ Go to your computer's shell and type the following command :

```
git branch NAME_OF_BRANCH
```

### How to create new branch and switch new branch
+ If you want to create new branch after creating new brach, switch to new branch


```
git checkout -b NAME_OF_BRANCH
```

### How to change current branch
+ If you want to change current branch then following command :


```
git checkout NAME_OF_BRANCH
```

### How to merge one branch to another
+ If you merge to another branch then following command :


```
git merge NAME_OF_BRANCH
```

### How to add a remote repo
+ To add new remote


```
git remote add {REMOTE_NAME} {URL_HTTPS} || {URL_GIT}
```

+ After set new remote, view your remote properties :


```
git remote -v
```

### How to pull from remote
+ Pull from remote repositories to get all changes


```
git pull origin NAME_OF_BRANCH
```

### How to fetch from remote
+ Fetch data from remote


```
get checkout --track {REMOTE_NAME}/{NAME_OF_BRANCH}
```

### How to display log history
+ Commit history

```
git log
```
+ Which is show the difference introduced in each commit


```
git log -p
```

+ Description of output
  * **%s** Subject
  * **%ar** Author date, relative
  * **%h** Commit hash
  * **%an** Author name
  * **%ad** Author date
  * **%cn** Comitter name
  * Example code line :


  ```
  git log --pretty=format:"%cn %ar"
  ```


### How to commit changes
+ To add and commit all local changes in one command :


```
git add .
git commit -m "COMMENT TO DESCRIBE THE INTENTION OF THE COMMIT"
```

+ Also if you want to push commit changes following command line :


```
git push {REMOTE_NAME} {NAME_OF_BRANCH}
```

+ Note: Check [this](https://chris.beams.io/posts/git-commit/#seven-rules) and learn how to write a proper commit message

### How to rebase one branch to another
+ Before rebase make sure feature branch and master is up to date
+ This sample rebase master into feature branch

```
git checkout master
git pull
```

+ After update master branch now get back feature branch

```
git checkout {FEATURE_BRANCH_NAME}
git rebase -i master
```

+ After this command if two branches has conflict before push resolve the conflicts

```
git push --f {REMOTE_NAME} {NAME_OF_BRANCH}
```

+ Note: Check [this](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase) and learn how to rebase


### How to reset commit
+ Before start make sure unpushed commit have it
+ Check your branch status

```
git status
```

+ After the result you can obtain your commit id or you can show how many commit ahead in current branch

```
git reset --hard HEAD~[NUMBER]|[COMMIT_ID]
```

### How to delete local or remote branch
+ Before start make sure unpushed commit have it
+ If you want to delete local branch type the following command

```
git branch -d {NAME_OF_BRANCH}
```

+ If you want to delete remote branch type the following command

```
git push origin -delete {NAME_OF_BRANCH}
```

### Extract sha key from apk
+ Go to your apk file location
+ Extract apk file, open terminal in apk location and use this command : 
```
unzip {APK_NAME} -d {UNZIP_FILE_NAME}
```
+ Go to /META-INF/ANDROID_.RSA file (this file may also be CERT.RSA, but there should only be one .RSA file).
+ Use command : 

```
keytool -printcert -file ANDROID_.RSA
```

+ After this command you can get fingerprints 

### Create static web server for the get http request
+ First install the http-server

```
sudo npm install -g http-server
```

+ After installed http server create new folder
+ Create new .json file inside the folder
+ {FILE_NAME}.json and add json text inside the document
+ Start http server using this command

```
http-server .
```
+ '.' means is read all file inside the folder
+ Http server will start on localhost

### Deploy apk remotely 
+ First connect device through usb 
+ Open terminal and set port, follow this command :

```
adb tcpip 5555
```

+ Now you can listen 5555 port while same network
+ You don't need to connect with usb 
+ Now connect to device via network

```
adb connect {DEVICE_INTERNAL_IP:PORT_NUMBER}
```

### GitLab and SSH key for Command Prompt
+ Go to your computer's shell and type the following command :
+ Mail adresses should be same as GitLab mail address


```
ssh-keygen -t rsa -C "your.email@example.com" -b 4096
```
+ Locating an existing SSH key


```
type %userprofile%\.ssh\id_rsa.pub
```
+ Open GitLab click on your **Avatar** and go to your **Profile Settings**

+ Navigate to **SSH keys**

+ Paste your SSH key to Box

![alt text](/images/ssh_key_paste.png)

+ Give **title** description

+ Final step is click to **Add Key**, also you can see fingerprint

### GitLab and SSH key for Linux / macOS
+ Go to your computer's shell and type the following command :
+ Mail adresses should be same as GitLab mail address
+ If you have SSH key then locate existing SSH key :


```
cat ~/.ssh/id_rsa.pub
```
+ If you see string starting with **ssh-rsa** you already have SSH key, if not you have to generate new SSH key follow the next step
+ Generating new SSH Key


```
ssh-keygen -t rsa -C "your.email@example.com" -b 4096
```
+ Open GitLab click on your **Avatar** and go to your **Profile Settings**

+ Navigate to **SSH keys**

+ Paste your SSH key to Box

![alt text](/images/ssh_key_paste.png)

+ Give **title** description

+ Final step is click to **Add Key**, also you can see fingerprint

# Install Android Studio on Windows
1. If you haven't install Android Studio follow the steps :
  * Go to [Android site](https://developer.android.com/studio/), dowload latest version Android Studio
  * Setup **android-studio-ide.exe**

# Follow Field Naming Conventions

+ Non-public, non-static field names start with m.

+ Static field names start with s.

+ Other fields start with a lower case letter.

+ Public static final fields (constants) are ALL_CAPS_WITH_UNDERSCORES.

```java
public class MyClass {
    public static final int SOME_CONSTANT = 42;
    public int              publicField;
    private static MyClass  sSingleton;
    int                     mPackagePrivate;
    private int             mPrivate;
    protected int           mProtected;
}
```

# Install Android Studio on Linux
1. If you haven't install Android Studio follow the steps :
  * Go to [Android site](https://developer.android.com/studio/), dowload latest version Android Studio
  * Unpack the .zip file you downloaded
  * Open a terminal, navigate to the **android-studio/bin/** directory, and execute **studio.sh.**
  * Select whether you want to import previous Android Studio settings or not, then click **OK.**

# Install Android Studio on MacOS
+ If you haven't install Android Studio follow the steps :
  * Go to [Android site](https://developer.android.com/studio/), dowload latest version Android Studio
 * Launch the **Android Studio** DMG file.
 * Drag and drop Android Studio into the Applications folder, then launch Android Studio.
 * Select whether you want to import previous Android Studio settings, then click **OK.**
 * The Android Studio Setup Wizard guides you though the rest of the setup, which includes downloading Android SDK components that are required for development.

# Project Configuration
+ After setup Android Studio follow the steps below :
  * Open **SDK Manager** from Android Studio, click **Tools>SDK Manager** or click **SDK Manager** ![alt text](/images/toolbar-sdk-manager.png) in the toolbar
  * Select API 27 and API 19
  * After select SDK platform click **SDK Tools**
  * Must be select **Google Play services**, **Android SDK Build Tools**, **Android Emulator** and **Android SDK platform Tools**
  * After selected items click **Apply** and  **Ok** close window
