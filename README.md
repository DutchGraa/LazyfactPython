##LazyFact##
######Factoring RSA moduli using crazy luck######

Lazyfact tries to factorise a RSA modulus using very basic methods.
This project is created for educational purposes and covers the following subjects:
- C, GMP
- C, OpenSSL
- Python, C extensions/packaging
- Python, threading using Queue
- Semiprime integer factorisation
	- Trial division
	- Pollards rho
	- Shanks squares
	- Findings another semiprime with a common GCD

	**Usage - building/installing**

$ cd src
$ sudo python setup.py install

	**Usage - using**

$ cd tryOut
$ gcc generator.c -o generator -lgmp -lcrypto 
$ ./generator > moduli.txt
$ python lazyfactThreading.py

	**Sources**

Factoring RSA moduli (semiprime integer factorisation)
	https://en.wikipedia.org/wiki/Integer_factorization#Factoring_algorithms
	https://class.coursera.org/crypto-010/lecture/preview

GMP
	https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library
	https://gmplib.org/manual/Integer-Functions.html#Integer-Functions
OpenSSL
	https://www.openssl.org/docs/manmaster/crypto/RSA_generate_key.html

Python threading using Queue
	https://docs.python.org/2/library/queue.html

Creating a Python C extension and packaging
	https://docs.python.org/2/extending/extending.html#providing-a-c-api-for-an-extension-module
	https://docs.python.org/2/extending/building.html#building
	https://docs.python.org/2/distutils/apiref.html#distutils.core.setup
	For C extension/threading GIL locking:
	http://jessenoller.com/blog/2009/02/01/python-threads-and-the-global-interpreter-lock

Licensing
	http://creativecommons.org/choose/