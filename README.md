# dsa_pratcie
def count_digits(n):
    n = abs(n)
    count = 0
    if n == 0:
        return 1
    while n > 0:
        count += 1
        n //= 10
    return count

print(count_digits(12345))
# countprime
class Solution(object):
    def countPrimes(self, n):
        if n < 3:
            return 0
        
        is_prime = [True] * n
        is_prime[0] = is_prime[1] = False
        
        for i in range(2, int(n ** 0.5) + 1):
            if is_prime[i]:
                for multiple in range(i * i, n, i):
                    is_prime[multiple] = False
        
        return sum(is_prime)
#all divider of a number
def all_divider_num(n):
    for i in range(1,n+1):
        if n%i==0:
            print(i)
        else:
            continue
n=int(input("enter a number:"))
all_divider_num(n)
#factorial
def factorial(n):
    N=1
    for i in range(1,n+1):
        N=N*i
    print(N)
n=int(input())
factorial(n)
#Fibonacci
