# -*- coding: utf-8 -*-
import multiprocessing as mp
#this is the fibonacci funtion
def fib(n):
    if n <= 2:
        return 1
    else:
        return fib(n-1)+fib(n-2) 

#this make the factorization
def factori(n):
  divisor=2
  if n <= 5:
    print(F[0],end="")
  else:
    while(n != 1):
      if n % divisor == 0:
        print(divisor,end="")
        n= n/divisor
        if n != 1:
          print("X",end="")
      else:
        divisor+=1

p =  mp.Pool(mp.cpu_count())
F=[]
count = 0

while(count <= 300):
  F = (p.map(fib,[count]))
  print(count,": ", F[0] ,":",end="")
  factori(F[0])
  print()
  count = count + 1
  print(count)