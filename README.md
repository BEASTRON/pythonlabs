# pythonlabs

#recursion
#! /usr/bin/env python3

#Bernardo D. Villajuan
#April 28, 2015
#recursiveBinarySearch.py



def main():
    numbers = [0, 1, 3, 4, 5, 10, 12, 13, 15, 16]
    low = 0
    high = len(numbers)-1
    while True:
        number = input("Enter a number: ") 
        if number == "":
            break
        result = recBinSearch(eval(number), numbers, low, high)
        if result == True:
            print(number, "was in the list.")
        else:
            print(number, "was not in the list.")
        
def recBinSearch(y, nums, low, high):
    if low > high:
        return -1
    mid = (low + high) // 2
    items = nums[mid]
    if items == y:
        return True
    elif y < items:
        return recBinSearch(y, nums, low, mid - 1)
    else:
        return recBinSearch(y, nums, mid + 1, high)
        
        
        






