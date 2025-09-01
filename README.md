# Experiment-5
## AIM:Write a python program for Binary Search and inspect for failures. 

# ALGORITHM
Start the program.
2. Get the list from the user
3. Get the element to be searched
4. Compare the mid element with the key, if same return the index
5. If key is greater, search it in the right side, else search it in the left side.
6. If not found return -1
 7. Stop the program. 

 # PROGRAM

 ```
def is_sorted(arr):
   return all(arr[i] <= arr[i+1] for i in range(len(arr)-1))

def binary_search(arr, key):
   low, high = 0, len(arr) - 1
   while low <= high:
       mid = (low + high) // 2
       if arr[mid] == key:
           return mid
       elif key > arr[mid]:
           low = mid + 1
       else:
           high = mid - 1
   return -1


arr = list(map(int, input("Enter list elements: ").split()))
key = int(input("Enter element to search: "))


if not is_sorted(arr):
   print("Failure: Binary Search requires a sorted array. The given array is not sorted.")
else:
   result = binary_search(arr, key)
   if result != -1:
       print(f"Element found at index {result}")
   else:
       print("Element not found")
```

 # OUTPUT

 <img width="728" height="85" alt="Screenshot 2025-09-01 111139" src="https://github.com/user-attachments/assets/671b01bf-2bb3-42a1-b4e3-bdad0a91bba3" />

 <img width="1100" height="78" alt="Screenshot 2025-09-01 111206" src="https://github.com/user-attachments/assets/a080fd52-67e1-47a3-917d-76a39506060f" />

 # RESULT
Thus,to write a python program for Binary Search and inspect for failures and the output is verified successfully.
