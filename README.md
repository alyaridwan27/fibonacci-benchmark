# Fibonacci
For this assignment, using the iterative and recursive approach to the sequence of fibonacci, I will compare the time and space complexity based on the results of the algorithm.
### Iterative Approach
```
int fibonacciIterative(int N){
    int num1 = 0, num2 = 1, numN;
    if (N==0){
        return num1;
    } else if(N==1){
        return num2;
    } else{
        for (int i = 2; i <= N; i++){
            numN = num1 + num2;
            num1 = num2;
            num2 = numN; 
        }
        return numN;
    }
}
```
### Recursive Approach
```
int fibonacciRecursive(int N){
    if (N==0){
        return 0;
    } else if (N==1){
        return 1;
    } else{
        return fibonacciRecursive(N-1) + fibonacciRecursive(N-2);
    }
}
```
# Testing
To test whether all inputs result in correct ouputs we must conduct a test.

### How To Run
In your terminal you can use the command below:
```
make; ./main_test.out
```
After running the command you should see this as an output:

<img width="809" alt="Screen Shot 2022-11-26 at 22 09 52" src="https://user-images.githubusercontent.com/114371692/204095712-13cd570b-1d0c-4f35-9a26-e43f41376675.png">

From running the test above we can see that the output is correct.

<img width="647" alt="Screen Shot 2022-11-26 at 22 11 52" src="https://user-images.githubusercontent.com/114371692/204095805-4fea1daa-f758-4a8f-871f-9f5464bf5c47.png">

# Benchmark
To compare the time and space complexity of both approach.
## Time Complexity
To check the execution time, I run N=10 for both iterative and recursive approach.
### How To Run
In your terminal you can use the command below:
```
make time
```
You should then see this as an output:

<img width="690" alt="Screen Shot 2022-11-26 at 22 26 38" src="https://user-images.githubusercontent.com/114371692/204096394-444ae48b-f228-4857-9a1d-05ef8f301c2e.png">

You can see that the time used for N=10 is 0.000004 for recursive and 0.000002 for iterative.

## Space Complexity
To check the memory usage, I run an infinite loop with N=1000. With a relatively huge N, I could see the memory usage for each function in the activity monitor.
### How To Run
In your terminal you can use these commands below:
```
make space
./main_b_space_iterative.out
```
```
make space
./main_b_space_recursive.out
```

