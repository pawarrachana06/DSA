# DSA ALGORITHM

## TIME AND SPACE COMPLEXITY

#### TIME COMPLEXITY

Not the actual time taken to run the program on machine (Its not machine dependent as the program might take different time on diffrent OD or platform eg Leetcode server based).It is the amout of time taken as function of input size(n)

No of operation changes as n increases.
NOTE: we consider worst case , since if x algorithm works with 10T users perfectly , certsinly it will work for 10 users.

#### SPACE COMPLEXITY
Amout of space taken by an algorithm as function of input size (n)

code : 1. Input space (vector, array , string)
       2. Auxiliary space ( extra space )

We consider only auxiliary space
       


#### BIG 0 NOTATION

The symbol we give for a number , displays its power 
eg: $5 and ₹5 

Different notations

1. Big O (worst case/upper bound)  (Consider the highest term) eg n^2 +n+5 =O(n^2)

2. Theta (θ)  Average case

3. Omega (Ω) (lower bound / best case)

#### BEST TO WORST TIME COMPLEXITY   

![image](https://github.com/user-attachments/assets/af101c7a-16a1-42a0-9da1-17b0f48382f7)

eg: sum of numbers from 1 to N

1. O(1) : No matter the n is large or small , same No of operation  will be performed.



``` Cpp
int n;
cin >> n;
int ans =n *(n+1)/3

```

2. O(n)

factorial sort
``` cpp
int fact=1;
for(int i=1;i<=n;i++){
fact*=i;
}
```

3. O(n^2) & O(n^3)

bubble sort
``` cpp
for (int i=0;i<n-1;i++){
for(int j=0;j<n-i-1;j++){
if(arr[j] > arr[j+1]) {
swap(arr[j],arr[j+1]);
}
}
}

```


4 . O(log n)
Binary search /BST

``` cpp
int s=0,e=n-1;
while(s<=e){

int mid=s+(e-s)/2;
if(arr[mid]<target){
s=mid+1;
}
else if(arr[mid]>target){
e=mid+1;
}
else{
return mid;}
}


```

5. O(nlogn)
 sorting
merge sort

6. O(2^n) & O(n!) (Worst than O(2^n)
 Recursion



  

   











