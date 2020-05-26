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