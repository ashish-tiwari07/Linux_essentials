## Basic Commands

1. **pwd** (present working directory) -> This command will help you know your present location in shell 



2. **cd** (change directory) -> This command will help you naviagte through diffrent directories and change your loaction 

    USE ->  

   
             cd ..               ( to go back to previous  directory )
            
             cd /home/ubuntu     ( go to a certain location directly )
    


3. **man**-> This command helps you to know about any command which you will working throughout your linux lifecycle

    USE -> 

             man cd               ( this will provide you more information about cd command )
  


4. **ls** (list) -> This command will help you to list out all files ,directories and stuff present over there 

    USE -> 

             ls                   ( list of files and directories )

             ls -a                ( this flag in ls command will help you to list out all hidden files as well {hidden files start will . } )

             ls -l                ( list everything along with details )  



5. **cat** (concatinate) -> this command will help you in viewing the content inside a file , making a new file along with the content to be written and append the content within a file as well.

    USE -> 

             cat readme.txt            ( this will help you to view the content inside a file )

             cat > hello.txt           ( it will create a new file named as hello.txt and will let you enter the content NOTE : after completion of typing press enter and then ctrl+D )    

             cat >> hello.txt          ( using >> in cat command you can add content to previous existing one )     

             cat file1 file2 > file3   ( used to concatinate contnet of file1 and file2 to file 3 ) 
     
    NOTE :-  (>)    single arrow will remove existing content and will write new one
                 (>>)   double arrow will help in addtion of content after existing one
           

    
6. **echo** -> mainly used to see whatever user writes after the command , Also can be used to alter the content in the file

    USE -> 

             echo HYY                           ( HYY will be displayes in shell )

             echo hy!! I am learning > file1    ( messege will be passed into file1 )
 


7. **tr** (Translate) -> used to translate characters in upper or lower case 

    USE-> 

             cat file.txt | tr a-z A-Z > upper.txt
             ( this command will firstly fetch the content from file.txt and then convert all the lower to upper case and finally will save it in upper.txt file )
    
    NOTE :- ( | ) this is known as "pipe" and is used to pass result of one command to the other specified commands

---

## File Handling Commands



8. **mkdir** (make directory) -> this command is used to make a new folder 

    USE ->

             mkdir movies               ( a new folder named "movies" will appear )

    NOTE :- rmdir command can be used to remove an "empty folder one" 

9. **touch** -> this command is used to make a new file or to update the time stamp of existing folder 

    USE -> 

             touch file1.txt            ( file.txt named file will be made in present directory )



10. **cp** (copy) -> this command is used to copy file or folder 

    USE -> 
    
             cp file1.txt file2.txt     ( file2.txt is a copy of file1.txt )

             cp -R folder1 folder2      ( folder1 is a copy of folder2 )
    
    NOTE :- if a particular location is not specified new file will be made in the present working directory 


 
11. **mv** (move) -> used to move file from one loaction to another and to rename the file 

    USE -> 

             mv file1 /home/ubuntu      ( file1 will move to /home/ubuntu folder )
             mv file1 file2             ( if a location is not specified and file2 doesn't exist , file1 will be renamed as file2 )



12. **rm** (remove) -> as name suggest this cmd is used to remove file and folder

    USE -> 

             rm file1.txt                ( file1.txt will be removed )
             rm -r/rm -R                 ( used to remove folder recursively )
             rm -rf                      ( to remove file or folder forcefully )



13. **head** -> used to view only few top lines of any file 

    USE -> 

             head -4 file.txt / head -n 4  file.txt        ( both of them will show tops 4 line of file.txt )
            


14. **tail** -> used to view last few line of any file

    USE ->

             tail -4 file.txt / tail -n 4 file.txt          ( both of them will show bottom 4 line of file.txt )

        
15. **diff** -> This command is used to compare two files line by line 

    USE -> 

             diff file1 file2             



16. **locate** -> Used to find files in whole system 

    USE ->

             locate "file.txt"             ( it will find out file.txt in system )
             
             locate "*.txt"                ( * here means anything can come in this place known ad WILDCARD )

            
17. **find** -> This command is also used to find file and folder with more precision

    USE -> 

             find . -type f -name "*.txt"
             ( this means find in current directory whose type is file and name which starts with anything but ends with .txt extension )



18. **grep** ( global regular expression print ) -> THE most important command while working with linux which basically is used to find text written in a file 

    USE -> 

             grep ash file.txt              ( it will fetch each word with "ash" as initial )
             
             grep -n ash file.txt           ( it will tell you line no. in which these words are used )

             grep -c ash file.txt           ( display no. of time the word is used in file )

    NOTE -> WILCARDS can be used ( discussed later in module )



19. **history** -> it will print all the commands that are recently used 


20. **vi/vim** -> this is an alternative editor used to insert text in file 
    USE ->   
    
            STEPS :-
             vi file1        -> to enter into vi editor 

             press i         -> to start entering your data 
  
             press esc       -> once you are finished 

             press :wq       -> to write ,save and quit 


    NOTE :- use  
    1.  :q! -> quit without saving changes 

    2.  :q  -> if not changes made 



 
21. **chmod** ->  this command is used to changes the permission of file 


             ls -al               ( this will give you details about permission granted to user , group and others )
             
             -rw-rw-r--  1 ubuntu ubuntu    0 Jul 11 19:56 file1
             -rw-rw-r--  1 ubuntu ubuntu    0 Jul 11 19:56 file2

    NOTE :- 
    1. first (-) represent if it is file or directory ( d menas directory )

    2. next 3 (-) represents permission granted to user
    
    3. next 3 (-) represents permission granted to groups
    
    4. next 3 (-) represents permission granted to others
            
            r = read , w = write , x = execute 

            values -> r = 4  , w = 2   , x =1 

    USE -> 

             chmode 745 file1                   ( 7 means user have all permission , 4 means read only to group and 5 means read and execute to others )

             chmod u=wr,g=r,o=wrx file1         ( another simple way to grant permissions )

             chmod +r/-r file1                  ( used to add add/remove read permission form all there entities )


22. **chown** (change owner) -> This command is used to the owner of any file

    USE -> 

             chown ashish file.txt               ( change owner of file.txt to ashish )

    NOTE :- use SUDO if permission is denied



## Networking Commands


23. **hostname** -> to get name of the host machine

    USE -> 

             hostname hplaptop                    ( to temporaty change the hostname to hplaptop )

             hostname -i                          ( to figure out the IP address of hostmachine )

24. **useradd** && **userdel** -> to add or delete user 
    USE-> 

             useradd ashish                        ( new user named ashish will me formed )

             userdel ashish                        ( to delete user named ashish )

    NOTE :- if home directory is not made use flag -m and -C to get complete user space 


25. **passwd** -> to upadte the password of user 

    USE -> 

             passwd ashish                          ( to setup new password for user ashish )


        
26. **du** -> to get disk usage by current files


27. **df** -> to get disk usage by all files 


28. **top** -> used to get the detailed information of application running on linux ( real-time display )

        NOTE :- press q to exit 


29. **ps** -> alternative of top command but doesn't run in real time 

    USE -> 
             
             ps -ef / ps -lf                        ( to get detail of every process )

             ps -aux / ps -axo                      ( will get cpu % also )

30. cat /etc/os-release -> to get all information about Operating System

31. **wget** -> used to download files or pdf thorugh URL 

    USE -> 
             
             wget [https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.simplilearn.com%2Fimage-processing-article&psig=AOvVaw15XSyZYk8ielMM7WD_BYwT&ust=1720797036076000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCPDAu9Kin4cDFQAAAAAdAAAAABAJ]()








