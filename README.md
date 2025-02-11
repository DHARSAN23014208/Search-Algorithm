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
Program for linear search method to match the item in a list
Developed by:DHARSAN KUMAR R
RegisterNumber: 23014208

def linearSearch():
    array=eval(input())
    array.sort()
    print(array)
    find=int(input())
    check=0
    index=0
    sum=0  
    for i in array:
        if(i==find):
             index=sum
             check=1
             break
        sum+=1
    if(check==1):
        print(f"Element found at index:  {index}")
    else:
        print("Element not found")
linearSearch()
        
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:dharsan kumar r
RegisterNumber: 23014208
'''
def binarySearchIter(array, l, u, find):
    while l<=u:
        mid=l+(u-l)//2
        if(array[mid]==find):
            return mid
        elif(array[mid]<find):
            l=mid+1
        else:
            u=mid-1
    return 0        
array=eval(input())
array.sort()
u=len(array)-1
f=int(input())
x=binarySearchIter(array,0,u,f)
print(array)
if(x==0):
    print("Element not found")
else:
    print(f"Element found at index:  {x}")

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Program to find the element in a list using Binary Search (recursive Method).
Developed by: dharsan kumar r
RegisterNumber: 23014208
def BinarySearch(array,find,l,u):
    if l<=u:
        mid=l+(u-l)//2
        if(array[mid]==find):
            return mid
        elif(array[mid]<find):    
            l=mid+1
            return BinarySearch(array,find,l,u)
        else:
            u=mid-1
            return BinarySearch(array,find,l,u)
    return -1    
arr = eval(input())
arr.sort()
k = eval(input()) 
l=0
h=len(arr)-1
x=BinarySearch(arr,k,l,h)
print(arr)
if(x==-1):
    print("Element not found")
else:
    print(f"Element found at index:  {x}")

```
##  Output
![image](https://github.com/DHARSAN23014208/Search-Algorithm/assets/149365413/e72a6902-58e7-4f10-b4b4-d658c95c8987)
![image](https://github.com/DHARSAN23014208/Search-Algorithm/assets/149365413/1819848d-0f5c-454b-9b6c-ccb8050de4cf)
![image](https://github.com/DHARSAN23014208/Search-Algorithm/assets/149365413/899caa15-9aee-4c0c-8e9b-7d22b3b2cb3a)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
