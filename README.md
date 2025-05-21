# 1. Function to add integer values of an array
def array_sum(arr):
    total = 0
    for i in range(len(arr)):
        total = total + arr[i]
    return total

# 2. Function to calculate average value of an array
def array_average(arr):
    total = 0
    count = 0
    for val in arr:
        total += val
        count += 1
    return total / count if count != 0 else 0

# 3. Function to find index of an element (first occurrence)
def find_index(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1  # Not found

# 4. Function to test if array contains a specific value
def contains_element(arr, target):
    for i in arr:
        if i == target:
            return True
    return False

# 5. Function to remove a specific element from array
def remove_element(arr, target):
    result = []
    found = False
    for i in arr:
        if i == target and not found:
            found = True
            continue
        result.append(i)
    return result

# 6. Function to copy array to another array
def copy_array(arr):
    new_arr = []
    for i in arr:
        new_arr.append(i)
    return new_arr

# 7. Function to insert element at specific position
def insert_element(arr, value, position):
    result = []
    for i in range(len(arr) + 1):
        if i < position:
            result.append(arr[i])
        elif i == position:
            result.append(value)
        else:
            result.append(arr[i - 1])
    return result

# 8. Function to find minimum and maximum values
def find_min_max(arr):
    min_val = arr[0]
    max_val = arr[0]
    min_index = 0
    max_index = 0
    for i in range(1, len(arr)):
        if arr[i] < min_val:
            min_val = arr[i]
            min_index = i
        if arr[i] > max_val:
            max_val = arr[i]
            max_index = i
    return min_index, max_index

# 9. Function to reverse an array
def reverse_array(arr):
    reversed_arr = []
    for i in range(len(arr)-1, -1, -1):
        reversed_arr.append(arr[i])
    return reversed_arr

# 10. Function to find duplicate values
def find_duplicates(arr):
    duplicates = []
    for i in range(len(arr)):
        for j in range(i + 1, len(arr)):
            if arr[i] == arr[j] and arr[i] not in duplicates:
                duplicates.append(arr[i])
    return duplicates

# 11. Function to find common values between two arrays
def find_common(arr1, arr2):
    common = []
    for i in arr1:
        for j in arr2:
            if i == j and i not in common:
                common.append(i)
    return common

# 12. Function to remove duplicate values
def remove_duplicates(arr):
    result = []
    for val in arr:
        exists = False
        for unique in result:
            if val == unique:
                exists = True
                break
        if not exists:
            result.append(val)
    return result

# 13. Function to find second largest number
def second_largest(arr):
    first = second = float('-inf')
    for i in arr:
...         if i > first:
...             second = first
...             first = i
...         elif i > second and i != first:
...             second = i
...     return second
... 
... # 14. Function to count even and odd numbers
... def count_even_odd(arr):
...     even = 0
...     odd = 0
...     for i in arr:
...         if i % 2 == 0:
...             even += 1
...         else:
...             odd += 1
...     return even, odd
... 
... # 15. Function to get difference between largest and smallest
... def diff_max_min(arr):
...     min_val = arr[0]
...     max_val = arr[0]
...     for i in arr:
...         if i < min_val:
...             min_val = i
...         if i > max_val:
...             max_val = i
...     return max_val - min_val
... 
... # 16. Function to check for two specific elements
... def check_two_elements(arr, val1, val2):
...     found1 = False
...     found2 = False
...     for i in arr:
...         if i == val1:
...             found1 = True
...         if i == val2:
...             found2 = True
...     return found1 and found2
