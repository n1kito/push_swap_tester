# Push_swap tester

A simple tester I wrote to help me with my push_swap project.
The tester is divided in two scripts that can also be used separately, allowing you to also simply generate random strings of numbers.

## Usage

Clone this repo directly into the folder where your push_swap executable is located.


```shell
git clone https://github.com/n1kito/push_swap_tester.git

chmod +x push_swap_tester.sh push_swap_num_gen.sh
```

### push_swap_tester.sh

If needed, open the script and change the path of you push_swap executable.

```shell
./push_swap_tester.sh $ARGUMENT 
# $ARGUMENT is the number of tests you want done.
```

### push_swap_num_gen.sh

```shell
./push_swap_num_gen $ARGUMENT
# $ARGUMENT is how many numbers you want generated.
```

### Using the number generator with the 42 Push_swap checker

```shell
ARG=$(../push_swap_tester/push_swap_num_gen.sh 500); ./push_swap $ARG | ./checker_MAC $ARG
# This will run your program on 500 numbers and pass it through the checker.

# If you want to see what numbers were tester (helpful if your algorithm fails):
ARG=$(../push_swap_tester/push_swap_num_gen.sh 500); ./push_swap $ARG | ./checker_MAC $ARG; echo $ARG

# If you want to make sure that the number generator worked correctly:
ARG=$(../push_swap_tester/push_swap_num_gen.sh 10); ./push_swap $ARG | ./checker_MAC $ARG; echo -n "Tested:"; echo $ARG | wc -w

# If you want both:
ARG=$(../push_swap_tester/push_swap_num_gen.sh 100); ./push_swap $ARG | ./checker_MAC $ARG; echo $ARG; echo -n "Tested:"; echo $ARG | wc -w
```

If you want to make sure that n numbers were actually tested:
```shell
ARG=$(../push_swap_tester/push_swap_num_gen.sh 500); ./push_swap $ARG | ./checker_MAC $ARG
# This will run your program on 500 numbers and pass it through the checker.
```