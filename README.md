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
```
''' 
Program for linear search method to match the item in a list
Developed by:Nishanth J
RegisterNumber:23007929
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
         return i
    return -1
array =eval(input())
k=eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
   


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:
RegisterNumber: 23007929
'''
def binarySearchIter(array, k, low, high):
    while low <= high:
        mid =low + (high - low)//2
        if array[mid] == k:
            return mid
            
        elif array[mid] < k:
            low = mid + 1
        else:
            high = mid - 1
    return - 1
array = eval(input())
array.sort()
k = eval(input())
result = binarySearchIter(array, k, 0, len(array)-1)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)





```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: your name
RegisterNumber: 
'''
def BinarySearch(arr, k, low, high):
    
    if high >= low:
        
        mid = low + (high - low)//2
        
        if arr[mid] == k:
            return mid
            
        elif arr[mid] > k:
            return BinarySearch(arr, k, low, mid-1)
            
        else:
            return BinarySearch(arr, k, mid+1,high)
    else:
        return-1
arr=eval(input())
arr.sort()
k=eval(input())
result=BinarySearch(arr,k,0,len(arr)-1)
if(result==-1):
   print(arr)
   print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)




```
## Sample Input and Output
![Screenshot 2023-12-31 214911](https://github.com/Nishanth-018/Search-Algorithm/assets/149347651/428b8f79-7819-4e32-b394-b200f661496a)
![Screenshot 2023-12-31 215050](https://github.com/Nishanth-018/Search-Algorithm/assets/149347651/bf064659-3560-44eb-897a-08e18c6bf6d4)
![Screenshot 2023-12-31 215209](https://github.com/Nishanth-018/Search-Algorithm/assets/149347651/fc27a156-8768-42b5-b9e8-ae32923f6e35)








## Result
Thus the linear search and binary search algorithm is implemented using python programming.
