# Project-6
Assignment 6
import os
clear = lambda: os.system("cls")
from math import *

def full_scholarship():
    clear()
    first_name = input("Enter First name: ")
    last_name = input("Enter Last name: ")
    fullnames = (first_name + " " + last_name)
    print("Fullnames: " + fullnames)
    country=input("Your Country? \nEnter A for Africa,or O for Oversees/Diaspora Coutries: ")
    Africa='A'
    Other_countries='O'
    if country==Africa:
        print("You are Eligible to Apply for Scholarships")
    else:
        print("Choose option 2 in the main menu!")
        print()
        menu()
    
    gender=input("Your Gender? \nEnter M for Male,or F for Female: ")
    Male='M'
    Female='F'
    if gender==Male:
        pass
    if gender==Female:
        pass
    else:
        print("Invalid Option")
    
    Student_ID=input("Student ID No: ")
    Phone_No=input("Student Telephone No: ")
    country=input("Country: ")
    city=input("City: ")
    mailing_address=input("Enter Mailing Address: ")
    
    
    quiz1 = eval(input("Please enter the score for Quiz 1: "))
    quiz2 = eval(input("Please enter the score for Quiz 2: "))
    quiz3 = eval(input("Please enter the score for Quiz 3: "))
    test1 = eval(input("Please enter the score for Test 1: "))
    test2 = eval(input("Please enter the score for Test 2: "))
    total= quiz1 + quiz2 + quiz3 + test1 + test2
    average=total/5
    print("The average is", round(average, 2))
    
    Zoom_Calls = eval(input("Please enter the score point for Zoom Calls: "))
    if Zoom_Calls > 9:
        print("Invalide number. Chooce 1 to 10 only")
        menu()
    
    Home_work = eval(input("Please enter the score points for the Home Work Assignment: "))
    if Home_work > 10:
        print("Invalide number. Chooce 1 to 10 only")
        menu()
        print("Thanks for your Application")
    
    if 90<=average<=100:
        print("Cogratulation! Youqualified for the scholarship")
        return 'A'
    elif 80<=average<=89:
        print("Cogratulation! You qualified for the scholarship")
        return 'B'
    elif 70<=average<=79:
        print("Cogratulation! qualified for the scholarship")
        return 'C'
    elif 60<=average<=69:
        print("Cogratulation! You Qualified for the scholarship")
        return 'D'
    elif 1<=average<=59:
        print("You have NOT Qualified for the scholarship")
        return 'E'
    else:
        return 'F'
        print("You DO NOT Qualified for the scholarship")
 
    input("Press enter for menu")
    menu()
    
def patial_scholarship():
    clear()
    print("This scholarship is not available")
    input("Press enter for menu")
    menu()

def exit():
    clear()
    input("Thanks for your Application!!")

def menu():
    clear()
    print("SCHOLARSHIP PROGRAMME")
    print("1. Full Scholarship")
    print("2. Patial Scholarship")
    print("3. Exit")
    choice=input("Enter the choice: ")
    if choice == "1":
        full_scholarship()
    elif choice=="2": 
        patial_scholarship()
    elif choice=="3":
        exit()
    else:
        clear()
        input("Wrong input. Press Enter for menu")
        menu()
menu()
