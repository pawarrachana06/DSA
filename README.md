# DSA ALGORITHM

## TIME AND SPACE COMPLEXITY

#### TIME COMPLEXITY

Not the actual time taken to run the program on machine (Its not machine dependent as the program might take different time on diffrent OS or platform eg Leetcode server based).It is the amout of time taken as function of input size(n)

No of operation changes as n increases.
NOTE: we consider worst case , since if x algorithm works with 10T users perfectly , certainly it will work for 10 users.

#### SPACE COMPLEXITY
Amout of space taken by an algorithm as function of input size (n)

code : 
1. Input space (vector, array , string)

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

### PROBLEMS 

1. Prime numbers

``` cpp
for(int i=2;i*i<= n;i++)
{
if(n%i ==0)
{
cout << "Non prime"
break;
}
}
```

Time complexity : O(√n)
the loop will run till i^2=n --> i=√n

O(√n) < O(n)

2. Selection sort

``` cpp

for(int i=0;i<n-1;i++)
{
int minIdx=i;
for (int j=i+1;j<n;j++)
{
if(arr[j]<arr[minIdx])
{
minIdx=j;
}
}

swap(arr[i],arr[minIdx]);

}

```

Time complexity = n *n =O(n^2)
  
3. Recursion

``` cpp

int factorial(int n)
{

if(n==0)
{
return 1
}
return n*factorial (n-1)

}
```

Time complexity methods

1.Recurrence relation
f(n)=k+f(n-1)=O(n)

![image](https://github.com/user-attachments/assets/e898df43-09fe-4632-9efb-1d0dcad7ba99)


2. Total No of recursion call * work done in each call

![image](https://github.com/user-attachments/assets/f679e9a5-8146-47d0-9746-398800d376bd)


space complexity 

stack occupies memory

SC= height of call stack * memory in each call
SC=O(n)
![image](https://github.com/user-attachments/assets/31404fdb-9c70-449a-93f0-be8ef7a3773f)


4. Recusrsive Fibonacci

``` cpp

int fib(int n)

{

if(n==0 || n==1)
{
return n;
}
return fib(n-1) * (n-2);
}

```
Time complexity:  O(2 ^n)


Space complexity : O(n)
![image](https://github.com/user-attachments/assets/61e73119-6015-484b-86c5-b1aa05b2c737)


![image](https://github.com/user-attachments/assets/b3589dfe-073c-4011-a6b0-47351ae6426e)

5. Merge sort

``` cpp

void mergrSort(int arr[],int si,int ei){

if(si>=ei)
{
return;
}
int mid=si+(ei-si)/2;
mergeSort(arr,si,mid);
mergeSort(arr,mid+1,ei);
merge(arr,si,mid,ei)
}

```

merge : TC O(n)  SC O(n)
![image](https://github.com/user-attachments/assets/b2fcc263-0341-4dbe-8264-b89bbbc4bfe8)

![image](https://github.com/user-attachments/assets/e31f7246-07e7-473a-b282-8cf781c64bad)

merge sort : TC o(n log n) SC 
![image](https://github.com/user-attachments/assets/9288559c-1d89-4044-aeea-3cef5cf32722)

![image](https://github.com/user-attachments/assets/69137881-767e-4bef-b94c-45f9013f491e)

### Code POV

![image](https://github.com/user-attachments/assets/2267f1c3-0f26-4014-9476-5100c74f71b5)

#### ! MOST IMPORTANT
![image](https://github.com/user-attachments/assets/c1af6b5d-0fca-4719-9a07-482b7cc818a8)







