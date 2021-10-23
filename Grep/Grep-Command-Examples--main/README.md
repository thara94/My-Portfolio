# Grep-Command-Examples-


After opening the ubuntu server, I used grep commands to find some expressions from a file called “datebook” which is located in the “CIS245” directory. The commands are shown in blue.
(Hint: to find the present working directory type “PWD”, to help you find your path)


1.	Grep “Street” and path. This command looks for all lines that contain Street and print them out.

 
![](https://user-images.githubusercontent.com/82772297/134829026-019e5465-818c-447f-97d3-02dca329ec11.png)


2.	Grep “^M” and path to print all lines the starts with uppercase M for the first names
 
![](https://user-images.githubusercontent.com/82772297/134830138-3948931c-c313-4d6a-8ec2-459bba084481.png)


3.	Grep “000$” and path. The command will print all lines the ends with “000”. The use of $ means at the end of the line.
 
![](https://user-images.githubusercontent.com/82772297/134830154-388c1efb-7c46-480f-b076-1fa785c9471a.png)


4.	Grep -v “408” and the path to print all lines that do not contain “408”. The use of -v means the opposite of.
 
![](https://user-images.githubusercontent.com/82772297/134830252-4ad59557-ad9d-4d83-981a-7a76e1e57aeb.png)

![](https://user-images.githubusercontent.com/82772297/134830278-b6b14cc3-8a9e-4173-911b-2bfbd4eca18a.png)


5.	Egrep “:[0-9]+\/[0-9]+\/23” and path to print all lines that have 1923 as a year of the birthday. This command looks for the semicolon, then a numbers between 0-9, and the + means more than one digit followed by /, then more than one-digit numbers between 0-9 followed by 23. 
 
![](https://user-images.githubusercontent.com/82772297/134830367-97ca1145-661b-47ee-8403-5983a4c8314e.png)


6.	egrep “:8..-[0-9]{3}-[0-9]{4}” and path to print all lines that have phone numbers of an area code that starts with 8. This command will look for the phone number by finding the:8 followed by the rest of the numbers. I used the regular expression [0-9] and {number} to present the numbers of the digits. 
 
![](https://user-images.githubusercontent.com/82772297/134830387-2f36e810-e00b-4923-b299-fda9691c2006.png)


7.	Egrep “[A-Z][a-z]\{5\}, [A-Z]” and path to print all lines that containing an uppercase letter, followed by 5 lowercase letters, followed by a comma, and an uppercase letter. I ran this command by using regular expressed [A-Z] for the uppercase letter, [a-z]\{5\} for the five lowercase letters, and[A-Z] for an uppercase letter.  
 
![](https://user-images.githubusercontent.com/82772297/134830412-1123ad8e-7a7f-4a5a-bce0-fe983ffef748.png)


8.	Egrep “[0-9]{4}:[0-9]{2,3} [A-Z]” and path to find lines that contain addresses that begin with  2 or 3 digit numbers. 
 The commands look for four places of numbers between zero to nine {0-9]{4} then looks for :, then  [0-9]{2,3} which means two or three digits numbers between zero and nine, and finally for an uppercase letter [A-Z]. 
 
![](https://user-images.githubusercontent.com/82772297/134830435-06209a16-4759-4f8d-bdcb-a5c24dd8945b.png) 


9.	Egrep -n “MA” and path to print all lines preceded by a line number for people from Massachusetts. The use of -n prints the line number of each number the has MA in it.

![](https://user-images.githubusercontent.com/82772297/134830677-33220136-2383-412f-978d-a4140400c274.png)


10.	Grep -v “Street” path | grep -v “St”. I used grep -v “Street “to print all lines that do not contain street, then I used the pipe to connect another command which is grep -v “St” and that will give me a result of all lines that do not contain Street or St.
 
![](https://user-images.githubusercontent.com/82772297/134830665-986f8d9f-77a9-43ac-af37-b69d6fe63482.png)
![](https://user-images.githubusercontent.com/82772297/134830706-6fd8f3d6-477e-4a9d-832a-7b94cb010c01.png)




References
https://flylib.com/books/en/4.356.1.25/1/

