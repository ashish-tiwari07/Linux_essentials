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
 

7. **tr** -> used to translate characters in upper or lower case 

    USE-> 

             cat file.txt | tr a-z A-Z > upper.txt
             ( this command will firstly fetch the content from file.txt and then convert all the lower to upper case and finally will save it in upper.txt file )
    
    NOTE :- ( | ) this is known as "pipe" and is used to pass result of one command to the other specified commandsss
        