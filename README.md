# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```python
''' 
Program for linear search method to match the item in a list
Developed by:B KRISHNAKANTH 
RegisterNumber: 23006762
'''
def linearSearch(array,n,k):
    for i in range(n):
        if array[i]==k:
            return i 
    return -1
    
array = eval(input())
array.sort()
k = eval(input())
n=len(array)
print(array)
result = linearSearch(array,n,k)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:B KRISHNAKANTH
RegisterNumber: 23006762
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
array.sort()
k = eval(input()) 
print(array)
result=binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by:B KRISHNAKANTH
RegisterNumber: 23006762
'''
def binarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return binarySearch(array, k,low,mid-1)
        else:
            return binarySearch(array, k, mid+1, high)
    else:
        return -1
        
    
    
array = eval(input())
array.sort()
k = eval(input()) # k is the element to be searched for
result=binarySearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)




```
## Output:

i)	#Use a linear search method to match the item in a list.
![image](https://github.com/Krishnakanth23006762/Search-Algorithm/assets/138849446/681b4bf8-51d3-4d05-907c-c55546c4cc0d)

ii)	# Find the element in a list using Binary Search(Iterative Method).
![image](https://github.com/Krishnakanth23006762/Search-Algorithm/assets/138849446/774bdb3e-3912-438d-bcb5-2e01a16fe6aa)

iii)	# Find the element in a list using Binary Search (recursive Method).

![image](https://github.com/Krishnakanth23006762/Search-Algorithm/assets/138849446/61ede780-86ca-4d8c-9120-97da0e7e539c)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
