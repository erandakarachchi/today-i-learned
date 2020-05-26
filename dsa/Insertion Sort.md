# Insertion Sort

Insertion sort is an in-place algorithm, which is used to sort data. This algorithm takes O(n<sup>2</sup>) time to sort the elements in the array. This is efficient for sorting small amount of data.

Assumption is made that left side in the list is already sorted. therefore we need to take the first unsorted value and then determine where to insert it.

sorted elements are shifted according to the determined position.

For an example, Consider the following array.



![ins_sort_unsorted](assets\ins_sort_unsorted.png)



### Step 01

In the step 01, We assume that left side of the array is sorted. Therefore we assume that 67 is in the sorted side. We take 45 as the first unsorted value and determines where to place it in the sorted side.

As 45 <= 67 , We move 45 before 67 and shift 67 to the right, After completing step 01, our array  looks like this.



![ins_step_01](assets\ins_step_01.png)

### Step 02

In this step, we take first element in the unsorted side, that is 23 and determine where to place it in the sorted side. 

As 25 <=45 and 25 <=67 , we move 25 to the beginning of  the sorted side and shift 45 and 67 to the right.

After the step 02, our array looks like this.

![ins_step_02](assets\ins_step_02.png)

### Step 03

In step 03, we take 89 as the key and determine where to place it in the sorted array. 

As 89 <=67 , we place 89 right next to 67 (no need to move as it is in the correct place.).

After the step 03, our array looks like this.

![ins_step_03](assets\ins_step_03.png)

### Step 04

In this step we take 12 as the key value, Then we compare it with the elements in the sorted array to determine where to place it.

As 12<=89 , 12<=67, 12 <=23 ,  we determine that we needs to place 12 as the first element of the array. Therefore we shift 45,67,89 to the right by 1.

After the step 04, our sorted array looks like this.

![ins_step-04](assets\ins_step-04.png)





## Insertion Sort Implementation (Python)

Here is the python implementation of insertion sort.

```python
def insertion_sort(number_list):
    '''
    always assumes left side of the key is already sorted.
    therefore we are checking where to place new key value in the sorted left side array.
    '''
    for i in range(1,len(number_list)):
        key = number_list[i] #as the loop starts from 1, assumes leftmost value is already sorted.
        j = i-1 #last index of the sorted sub array.
        while j >= 0 and number_list[j] >key: #loops from end of the sorted part to begining and determine where to place the key.
            number_list[j+1] = number_list[j] #while current_value_in_the_list > key, shift current value to the right.
            j = j-1
        number_list[j+1] = key #place the key in the new position after shifting values.
    return(number_list)

```

To test this algorithm, use the function as follows.

```python
print(insertion_sort([5,2,4,6,1,3]))
print(insertion_sort([45,65,87,54,867,54,7643,65,87]))
```

