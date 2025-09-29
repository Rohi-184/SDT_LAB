On the Command Prompt ( As Administrator ) : 
-----------------------------------------------


docker --version ( To check the version of Docker )


docker pull debian ( Used to pull the debian compiler from docker hub )


docker ps -a ( List All Containers )


docker run -it debian ( Run the Debian image )


apt update ( Update apt )


apt install nano ( install nano file editor )


apt install python3 ( install python change version as you need )


nano fibo.py ( open the file on nano editor )

Code :

def fibonacci_iterative(n):
    """Generate Fibonacci series up to the nth term using iteration."""
    sequence = []
    a, b = 0, 1
    for _ in range(n):
        sequence.append(a)
        a, b = b, a + b
    return sequence

# Example usage
n = 10
print(fibonacci_iterative(n))


python3 fibo.py ( run python program )
