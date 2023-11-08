# STUDENT-MANAGEMNET-SYSTEM
print('STUDENT MANAGEMENT SYSTEM ===>\
\n     BENEFITS\
\n===>improves general performance of the students.\
\n \
\n===>it would also help in minimal use of papers hence helping in  prevention of paper wastage\
\n \
\n===>it makes the manual labour of managing these recordes easy\
\n \
\n===>it works simply and streamlines all tasks\
\n \
\n===>improved communication\
\n \
\n===>can be accessed by all parties involved\
\n \
\n===>helps to keep track of all students\
\n\
\n===>reduction of human labour and workload\
\n\
\n===>provides a means to advice students\
\n\
\n===>improves the general comfort of the staff\
\n\
\n \====-HELPFUL BENFITS OF PYTHON-=========\
\n ====>it is versatile\
\n\====>easy to use\
\n\===>it is fast to develop\
\n\===> it is open source with a vibrant community\
\n\===>it has all the libraries you can imagine\
\n\===>great prototypes: you can do more by coding less')


global liststd
# creating a variavle inside a function
#making ListStd As super Global Variable i.e
# a variable inside and outide the functions


liststd= ['a','b','c', 'd','e','f','g','h',\
              'i','j','k','l','m']


global dict
# mutable data type
dict = {}
for name in liststd:            
    dict[name] = 0


global dict1
dict1 = {}
for name in liststd:            
    dict1[name] = ""


global dict2
dict2 = {}
for name in liststd:
    dict2[name] = ""


global dict3
dict3 = {}
for name in liststd:
    dict3[name] = ""


    
    
"""some dictionaries have been defined as
global in order to make use of it in the whole program"""


def main():
    
    #have to store the whole program so in 'main' so that it can run again
    
    import os
    
    #user and software interface
    import platform
    # to see the underlying platforms info or data
    


 
    
              # list of students


    def managestudent():
        # function for the student management system


        x= "#" * 30
        y= "=" * 28
        global bye
        bye='===>this program has ended<==='


    print('''
    ----------------------------------------------------------
    |---------------------------------------------------------|
    ===============STUDENT MANAGEMENT FILE=====================
    |----------------------------------------------------------|


    ______welcome_______


    enter 1: to view students' list
    enter 2: to add new student
    enter 3: to search student
    enter 4: to remove student
    enter 5: to make a new list of students
    enter 6: to view percentage of students
    enter 7: to enter percentage of student
    enter 8: to enter house of student
    enter 9: to view house of student
    enter 10: to enter bus routes of students
    enter 11: to view bus routes of students
    enter 12: to record entries of deposition of fees
    enter 13: to view entries of deposition of fees
     ''')


    #options for the user to choose from^
    
    userinput=int(input('select the one of the given options above :'))
    # user will select any of the options
    


    if(userinput==1) :
        
        print('list students\n')
        
        #will print the given sentence in the new line
        
        for students in liststd:
            print("- {}" . format(students))
                #it will print the list of students in the curly bracket
            


        j = input("Do you want to continue (YES / NO) - ").lower()
        #the input would be converted to lower case
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        #the program would be returned to the start
        else:
            print('''===============================================
                  ==================-system end-====================
                  ==========-thank you for using our system-========
                  ================================================''')
            exit()
          #asking the user to start again or end the program




            
    elif(userinput==2):
        
        #this option adds a new line
        g = int(input("Enter number of students you want to add in the list - "))
        for i in range (0,g):
            
            newStd = input('enter new student : ')
            l2 = list(newStd)
                
            if(newStd in liststd):
                #this condition would check if you are in the list before hand
                print('\n this student {} already in the database'.format(newStd))
                    #error message
            else:
                liststd.append(newStd)
                #add the student int he existing list
                print('\n=> new student {} successfully add \n'.format(newStd))
                #.format would print the names in the curly bracket
                
        for students in liststd:
            print('=. {}'.format(students))
            
                        
        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('''===============================================
            ==================-system end-====================
            ==========-thank you for using our system-========
            ================================================''')
            exit()
                        #asking the user to end the program or continue the program


                        
    elif(userinput==3):
        
        #this option will search student from the list
                srcStd= input('enter student name in search:')
                if(srcStd in liststd):
                    #this condition searching the student
                    print('\n=> record found of student {}'. format(srcStd))
                    print("Roll no. - ",liststd.index(srcStd) + 1)
                else:
                    print('\n => no record found of student {}'. format(srcStd))
                    # error message




                j = input("Do you want to continue (YES / NO) - ").lower()
                if j == 'YES' or j == 'yes' or j == 'Yes':
                    main()
                else:
                    print('''===============================================
                         ==================-system end-====================
                         ==========-thank you for using our system-========
                         ================================================''')
                    exit()
                        # asking the user to end or continue the program


                




    elif(userinput==4):
        
        #this option will remove student from the list
        rmStd= input('enter student name to remove : ')
        if (rmStd in liststd):
            # condition for removing the student from the list
            liststd.remove(rmStd)
            print('\n => student {} successfully deleted \n'.format(rmStd))
        else:
            print('student not found in the data base')


            
        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('''===============================================
                      ==================-system end-====================
                      ==========-thank you for using our system-========
                      ================================================''')
            exit()
                #asking the user to continue or end the program






    elif(userinput == 5):
        
        liststd.clear()
        #.clear function would remove all elements in the list
        dict.clear()
        #would clear the dictionary
        
        k = int(input("Enter number of students to be added in the list - "))
        for i in range (0,k):
            name = input("Enter name of student - ")
            liststd.append(name)
            #append function would add students in list
            print("Added\n")
        print("\nNew list = ",liststd)
        """ a new list has been created"""
        for name in liststd:            
            dict[name] = 0
            #name would be in place of index 0


        
        
        j = input("Do you want to continue (YES / NO) - ").lower()
        # .lower : any name that the userinputs would be in lowercase
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main() #main() is defined in the beginning of the code and would restart the code from the begining
        else:
            print('''===============================================
                     ==================-system end-====================
                    ==========-thank you for using our system-========
                    ================================================''')
            exit()
            #the code would end with exit(), it wsould exit the code
         #asking the user to continue or end the program






    elif(userinput==6):
        
        for i in sorted(dict.items(), key=lambda item: item[1],reverse = True):
             print(i)
             #sorted in descending order
            #lamda is a small function which can take any arguement or form but of only one expression 
        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
                print('''===============================================
                         ==================-system end-====================
                        ==========-thank you for using our system-========
                        ================================================''')
                exit()




                
    elif(userinput==7):


  
    # create an empty list 
    # Add student information to the list 
        
    
        count = int(input("Enter no. of students - "))
        for i in range(0,count):
            name = input("Enter student name -  ")
            per = int(input("Enter % -  "))
            dict[name] = per
          #dictionary has been created  




        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('''===============================================
                  ==================-system end-====================
                  ==========-thank you for using our system-========
                 ================================================''')
            exit()
                #asking the user to continue or end the program






    elif(userinput==8):
        
        dict1.clear()
        #dictionary has been cleared
        ct = int(input("Enter no. of students - "))
        for p in range(0,ct):
            name = input("\nEnter student name -  ")
            hou = input("Enter name of house -  ")
            dict1[name] = hou
            #this will print name of the student and house of the student as dictioanry has been created


        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('===============================================\
                  ==================-system end-====================\
                  ==========-thank you for using our system-========\
                  ================================================')
            exit()


            


            
    elif(userinput==9):
        
        for t in dict1:
            print(t, '-',dict1[t])
        #the names and houses are stored in 'dict1' so it will print the list of students and their respective houses
        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('===============================================\
                  ==================-system end-====================\
                  ==========-thank you for using our system-========\
                  ================================================')
            exit()


    elif(userinput==10):
        dict2.clear()
        ct = int(input("Enter no. of students - "))
        for p in range(0,ct):
            name = input("\nEnter student name -  ")
            rou = input("Enter bus route -  ")
            dict2[name] = rou
            #name and rou have been stored in dict2 and would print together


        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('===============================================\
                  ==================-system end-====================\
                  ==========-thank you for using our system-========\
                  ================================================')
            exit()




    elif(userinput==11):
        
        for name in dict2:
            print(name, '-',dict2[name])


        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('===============================================\
                ==================-system end-====================\
                ==========-thank you for using our system-========\
                ================================================')
        exit()




    
    elif(userinput==12):
        
        dict3.clear()
        ct = int(input("Enter no. of students - "))
        for p in range(0,ct):
            name = input("\nEnter student name -  ")
            fees = input("Fees (deposited/not deposited): -  ")
            dict3[name] = fees


        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('===============================================\
                  ==================-system end-====================\
                  ==========-thank you for using our system-========\
                  ================================================')
            exit()




    elif(userinput==13):
        for name in dict3:
            print(name, '-',dict3[name])
            #name is stored in dict3


        j = input("Do you want to continue (YES / NO) - ").lower()
        if j == 'YES' or j == 'yes' or j == 'Yes':
            main()
        else:
            print('===============================================\
                  ==================-system end-====================\
                  ==========-thank you for using our system-========\
                  ================================================')
            exit()




    elif(userinput < 1 or userinput > 13):
        print('please enter valid option')
        #error message
        runAgn= input('\n want to run again? yes/no').lower()
        #it will show in lower case inferior of what the user has made
        if(runAgn=='yes'):
            main()
            #it will restart the program
            
        else:
            print('''===============================================
                  ==================-system end-====================
                  ==========-thank you for using our system-========
                  ================================================''')
            exit()   


# in case the user entered a unknown option
# this is used to complete the defining of the program
#the whole code is defined in main()
#main()
