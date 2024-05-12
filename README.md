# Recipe_Recommender_System
This recipe recommender system is created by using Python
import pandas as pd
from openpyxl import load_workbook

print("WELCOME TO RECIPE RECOMMENDER")
print("\nSELECT CHOICES FROM BELOW\n1.INDIAN_VEGITERIAN\n2. INDIAN_NON_VEGITERIAN\n3.ITALIAN_VEGITERIAN\n4.ITALIAN_NON_VEGITERIAN\n5.DIBETIC_FRIENDLY")
ch=int(input("\nEnter choice from above:"))

if (ch==1):
    ing=eval(input("Enter the main ingredients you have more than two in []brackets seperated by comma(,)and within ('') :="))
    print("\ningredients you have enter are:",ing)
    df=pd.read_excel(r"C:\Users\saees\Desktop\IndianVeg.xlsx")
    
    end=len((ing))
    
    cell_value = [df.iloc[0, i] for i in range(1, 11)]
    
    match_count=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count += 1
    
    cell_value = [df.iloc[1, i] for i in range(1, 9)]
    match_count1=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count1+= 1
    
    cell_value = [df.iloc[2, i] for i in range(1, 7)]
    match_count2=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count2 += 1
    
    cell_value = [df.iloc[3, i] for i in range(1, 7)]
    match_count3=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count3 += 1
    
    cell_value = [df.iloc[4, i] for i in range(1, 12)]
    match_count4=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count4 += 1
    
    cell_value = [df.iloc[5, i] for i in range(1, 11)]
    match_count5=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count5 += 1
    
    cell_value = [df.iloc[6, i] for i in range(1, 9)]
    match_count6=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count6 += 1
    
    cell_value = [df.iloc[7, i] for i in range(1, 6)]
    match_count7=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count7 += 1
    
    cell_value = [df.iloc[8, i] for i in range(1, 7)]
    match_count8=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count8 += 1
    
    cell_value = [df.iloc[9, i] for i in range(1, 9)]
    match_count9=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count9 += 1
                   
    match_counts = [match_count, match_count1, match_count2, match_count3, match_count4, match_count5, match_count6, match_count7, match_count8, match_count9]
    names = [df.iloc[i, 0] for i in range(10)]  

    match_found = False
    for i in range(len(match_counts)):
        if match_counts[i] >= end - 1:  
            print("\nRECIPE YOU CAN MAKE AND ENJOY\n", names[i])
            match_found = True
            break

    if not match_found:
        print("SORRY, MATCH NOT FOUND")


elif (ch==2):
    ing=eval(input("Enter the main ingredients you have in []brackets seperated by comma(,)and within '':="))
    print("\ningredients you have enter are:",ing)
    df=pd.read_excel(r"C:\Users\saees\Desktop\Indian_Non_Veg1.xlsx")
    
    end=len((ing))
    
    cell_value = [df.iloc[0, i] for i in range(1, 11)]
    
    match_count=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count += 1
    
    cell_value = [df.iloc[1, i] for i in range(1, 10)]
    match_count1=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count1+= 1
    
    cell_value = [df.iloc[2, i] for i in range(1, 10)]
    match_count2=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count2 += 1
    
    cell_value = [df.iloc[3, i] for i in range(1, 10)]
    match_count3=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count3 += 1
    
    cell_value = [df.iloc[4, i] for i in range(1, 10)]
    match_count4=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count4 += 1
    
    cell_value = [df.iloc[5, i] for i in range(1, 10)]
    match_count5=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count5 += 1
    
    cell_value = [df.iloc[6, i] for i in range(1, 10)]
    match_count6=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count6 += 1
    
    cell_value = [df.iloc[7, i] for i in range(1, 11)]
    match_count7=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count7 += 1
    
    
    
    match_counts = [match_count, match_count1, match_count2, match_count3, match_count4, match_count5, match_count6, match_count7]
    names = [df.iloc[i, 0] for i in range(len(match_counts))]

    match_found = False
    for i in range(len(match_counts)):
        if match_counts[i] >= end - 1:
            print("\nRECIPE YOU CAN MAKE AND ENJOY\n", names[i])
            match_found = True
            break

    if not match_found:
        print("SORRY, MATCH NOT FOUND")

    
elif (ch==3):
    ing=eval(input("Enter the main ingredients you have in []brackets seperated by comma(,)and within '':="))
    print("\ningredients you have enter are:",ing)
    df=pd.read_excel(r"C:\Users\saees\Desktop\ItalianVeg.xlsx")
    
    end=len((ing))
    
    cell_value = [df.iloc[0, i] for i in range(1, 8)]
    
    match_count=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count += 1
    
    cell_value = [df.iloc[1, i] for i in range(1, 7)]
    match_count1=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count1+= 1
    
    cell_value = [df.iloc[2, i] for i in range(1, 6)]
    match_count2=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count2 += 1
    
    cell_value = [df.iloc[3, i] for i in range(1, 5)]
    match_count3=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count3 += 1
    
    cell_value = [df.iloc[4, i] for i in range(1, 7)]
    match_count4=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count4 += 1
    
    cell_value = [df.iloc[5, i] for i in range(1, 7)]
    match_count5=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count5 += 1
    
    
    
    match_counts = [match_count, match_count1, match_count2, match_count3, match_count4,match_count5 ]
    names = [ df.iloc[0, 0], df.iloc[1, 0], df.iloc[2, 0], df.iloc[3, 0], df.iloc[4, 0], df.iloc[5, 0]]

    found_match = False
    for i in range(len(match_counts)):
        if match_counts[i] == end or match_counts[i] == end - 1:
            print("\nRECIPE YOU CAN MAKE AND ENJOY\n",names[i])
            found_match = True

    if not found_match:
        print("SORRY MATCH NOT FOUND")

    
    
elif (ch==4):
    ing=eval(input("Enter the main ingredients you have in []brackets seperated by comma(,)and within '':="))
    print("\ningredients you have enter are:",ing)
    df=pd.read_excel(r"C:\Users\saees\Desktop\italian_nonveg.xlsx")
    
    end=len((ing))
    
    cell_value = [df.iloc[0, i] for i in range(1, 7)]
    
    match_count=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count += 1
    
    cell_value = [df.iloc[1, i] for i in range(1, 8)]
    match_count1=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count1+= 1
    
    cell_value = [df.iloc[2, i] for i in range(1, 10)]
    match_count2=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count2 += 1
    
    cell_value = [df.iloc[3, i] for i in range(1, 9)]
    match_count3=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count3 += 1
    
    cell_value = [df.iloc[4, i] for i in range(1, 6)]
    match_count4=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count4 += 1
    
    cell_value = [df.iloc[5, i] for i in range(1, 10)]
    match_count5=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count5 += 1
    
    
    match_counts = [match_count, match_count1, match_count2, match_count3, match_count4, match_count5]
    names = [ df.iloc[0, 0], df.iloc[1, 0], df.iloc[2, 0], df.iloc[3, 0], df.iloc[4, 0], df.iloc[5, 0]]

    found_match = False
    for i in range(len(match_counts)):
        if match_counts[i] == end or match_counts[i] == end - 1:
            print("\nRECIPE YOU CAN MAKE AND ENJOY\n",names[i])
            found_match = True

    if not found_match:
        print("SORRY MATCH NOT FOUND")

    
    
elif (ch==5):
    ing=eval(input("Enter the main ingredients you have in []brackets seperated by comma(,)and within '':="))
    print("\ningredients you have enter are:",ing)
    df=pd.read_excel(r"C:\Users\saees\Desktop\diabetic 1.xlsx")
    
    end=len((ing))
    
    cell_value = [df.iloc[0, i] for i in range(1, 5)]
    
    match_count=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count += 1
    
    cell_value = [df.iloc[1, i] for i in range(1, 6)]
    match_count1=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count1+= 1
    
    cell_value = [df.iloc[2, i] for i in range(1, 10)]
    match_count2=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count2 += 1
    
    cell_value = [df.iloc[3, i] for i in range(1, 7)]
    match_count3=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count3 += 1
    
    cell_value = [df.iloc[4, i] for i in range(1, 6)]
    match_count4=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count4 += 1
    
    cell_value = [df.iloc[5, i] for i in range(1, 6)]
    match_count5=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count5 += 1
    
    cell_value = [df.iloc[6, i] for i in range(1, 6)]
    match_count6=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count6 += 1
    
    cell_value = [df.iloc[7, i] for i in range(1, 6)]
    match_count7=0
    for elem1 in ing:
        for elem2 in cell_value :
              if(elem1== elem2):
                   match_count7 += 1
    
    
    match_counts = [match_count, match_count1, match_count2, match_count3, match_count4, match_count5, match_count6, match_count7]
    names = [ df.iloc[0, 0], df.iloc[1, 0], df.iloc[2, 0], df.iloc[3, 0], df.iloc[4, 0], df.iloc[5, 0], df.iloc[6, 0], df.iloc[7, 0]]

    found_match = False
    for i in range(len(match_counts)):
        if match_counts[i] == end or match_counts[i] == end - 1:
            print("\nRECIPE YOU CAN MAKE AND ENJOY\n",names[i])
            found_match = True

    if not found_match:
        print("SORRY MATCH NOT FOUND")

    
    

else:
    print("Please enter the valid choice from above menu")

    

rating_str = input("Please enter your rating (1-5): ")

try:
    rating = int(rating_str)
    if rating < 1 or rating > 5:
        raise ValueError("Rating should be between 1 and 5.")
    print("Thank you for your rating!")
except ValueError as e:
    print(e
