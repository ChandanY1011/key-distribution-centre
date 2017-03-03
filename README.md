This is an implementation of a "Key Distribution Centre" which generates and distributes a session key to two clients A and B.
The KDC already shares a symmetric session key with A and B.
The file KDC1.cpp is run on the KDC and the file AB1.cpp is run on the machines A and B.

The files use openSSL and Socket Programming.

How to run?
1. On KDC, run:
  g++ KDC1.cpp -lcrypto
  ./a.out <portno>
  
2. On A (the machine which needs to communicate with B), run:
  g++ AB1.cpp -lcrypto
  ./a.out
  initiate
  
3. On B (the machine which is ready to communicate with any device), run:
  g++ AB1.cpp -lcrypto
  ./a.out
  listen
