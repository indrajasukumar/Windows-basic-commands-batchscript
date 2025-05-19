# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT
![image](https://github.com/user-attachments/assets/637724d2-d2cb-4c91-b3a5-1e2e83b3403a)

Remove the directory "my-folder"

## COMMAND AND OUTPUT
![image-1](https://github.com/user-attachments/assets/569a5f94-cde2-462c-a2cf-d37afb527f51)


Create the file Rose.txt

## COMMAND AND OUTPUT

![image-2](https://github.com/user-attachments/assets/ec79f6b9-7670-441e-a3d2-79b24758b183)

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT
![image-3](https://github.com/user-attachments/assets/53ff5976-dfed-4c41-a354-fbe30ffad6c2)

Remove the file hello1.txt

## COMMAND AND OUTPUT
![image-5](https://github.com/user-attachments/assets/0c465f1e-c566-4bc4-8335-14b7fa067d14)

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT
![image-5](https://github.com/user-attachments/assets/e42471de-5e13-411a-9538-16dd1efab930)

List out all the associated file extensions 

## COMMAND AND OUTPUT

![image-18](https://github.com/user-attachments/assets/74c8f7ed-bc42-4aae-babc-3e48c3915846)
![image-19](https://github.com/user-attachments/assets/f01443fd-a95c-429a-b683-e935533380c2)
![image-20](https://github.com/user-attachments/assets/65c7522b-e77f-4674-8dfb-f83447fa1ee8)
![image-21](https://github.com/user-attachments/assets/6415991e-cc05-4845-a014-89fcc1555ee6)
![image-22](https://github.com/user-attachments/assets/37f65c5b-adff-4591-9574-f1ba1d050788)



Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".
```
@echo off
set name=John
echo Hello, %name%
pause
```




## OUTPUT
![image-9](https://github.com/user-attachments/assets/d670ff51-983c-4dc3-9935-aabad5d3bf58)



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:loop
set /p num=Enter a number: 
set /a rem=%num% %% 2

if %rem%==0 (
    echo %num% is Even
) else (
    echo %num% is Odd
)

:ask
set /p ans=Do you want to check another number? (Y/N): 
if /I "%ans%"=="Y" goto loop
if /I "%ans%"=="N" goto end
echo Invalid input. Please enter Y or N.
goto ask

:end
echo Thank you!
pause
```


## OUTPUT

![image-10](https://github.com/user-attachments/assets/e998a74a-086a-4fcd-a8aa-1d2b2bfa971b)



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

```
@echo off
for /L %%i in (1,1,5) do (
    echo Number: %%i
)
pause
```


## OUTPUT
![image-11](https://github.com/user-attachments/assets/b62e8852-9e28-49cd-8d51-c5055208f333)




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
## OUTPUT
![image-13](https://github.com/user-attachments/assets/a45dafeb-1a46-46a7-853c-a5c4ec5496e9)


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off
:menu
cls
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option (1-3): 

if "%choice%"=="1" goto hello
if "%choice%"=="2" goto create
if "%choice%"=="3" goto exit
echo Invalid choice.
pause
goto menu

:hello
echo Hello, World!
pause
goto menu

:create
echo This is a new file > newfile.txt
echo File newfile.txt created.
pause
goto menu

:exit
echo Goodbye!
pause
exit
```

## OUTPUT
![image-15](https://github.com/user-attachments/assets/9d0e4e55-0052-4e5d-a52f-06601e2efea9)
![image-16](https://github.com/user-attachments/assets/4d854626-9561-4b93-b9e8-d8d359d8c636)
![image-17](https://github.com/user-attachments/assets/f34d20d9-7c36-490c-b5b4-c1e0477a01d5)



# RESULT:
The commands/batch files are executed successfully.

