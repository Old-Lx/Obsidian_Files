# Decoradores
Decorators are flexible way to modify or extend behavior of functions or methods, without changing their actual code. [Decoradores en Python](https://www.geeksforgeeks.org/python/decorators-in-python/) 

![[Pasted image 20260515112232.png]]

![[Pasted image 20260515112419.png]]
![[Pasted image 20260515113638.png]]
![[Pasted image 20260515113808.png]]
![[Pasted image 20260515113950.png]]
![[Pasted image 20260515114031.png]]
![[Pasted image 20260515114212.png]]
![[Pasted image 20260515114319.png]]
![[Pasted image 20260515114504.png]]


![[Pasted image 20260515113118.png]]

## Recursividad
![[Pasted image 20260515114708.png]]

![[Pasted image 20260515114909.png]]
![[Pasted image 20260515115109.png]]
![[Pasted image 20260515115301.png]]
![[Pasted image 20260515115410.png]]



## Ejemplo:

``` Python
def decorator(func):
    def wrapper():
        print("Before calling the function.")
        func()
        print("After calling the function.")
    return wrapper

@decorator
def greet():
    print("Hello, World!")
greet()
```

