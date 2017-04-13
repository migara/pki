# README #


### What is this repository for? ###

* Quick PKI setup

### Dependencies ###

* OpenSSL

### Folder Structure ###

.
├── certs
│   └── ca.cert.pem
├── crl
├── index.txt
├── index.txt.attr
├── index.txt.old
├── intermediate
│   ├── certs
│   │   ├── ca-chain.cert.pem
│   │   ├── client1.cert.pem
│   │   ├── client2.cert.pem
│   │   ├── client3.cert.pem
│   │   ├── client4.cert.pem
│   │   ├── client5.cert.pem
│   │   ├── intermediate.cert.pem
│   │   └── www.example.com.cert.pem
│   ├── client1.pfx
│   ├── client2.pfx
│   ├── client3.pfx
│   ├── client4.pfx
│   ├── client5.pfx
│   ├── crl
│   │   └── intermediate.crl.pem
│   ├── crlnumber
│   ├── crlnumber.old
│   ├── csr
│   │   ├── client1.csr.pem
│   │   ├── client2.csr.pem
│   │   ├── client3.csr.pem
│   │   ├── client4.csr.pem
│   │   ├── client5.csr.pem
│   │   ├── intermediate.csr.pem
│   │   └── www.example.com.csr.pem
│   ├── index.txt
│   ├── index.txt.attr
│   ├── index.txt.attr.old
│   ├── index.txt.old
│   ├── newcerts
│   │   ├── 1000.pem
│   │   ├── 1001.pem
│   │   ├── 1002.pem
│   │   ├── 1003.pem
│   │   ├── 1004.pem
│   │   ├── 1005.pem
│   │   └── 1006.pem
│   ├── openssl.cnf
│   ├── private
│   │   ├── client1.key.pem
│   │   ├── client1.key.pem.withkey
│   │   ├── client2.key.pem
│   │   ├── client3.key.pem
│   │   ├── client4.key.pem
│   │   ├── client5.key.pem
│   │   ├── intermediate.key.pem
│   │   └── www.example.com.key.pem
│   ├── serial
│   └── serial.old
├── newcerts
│   └── 1000.pem
├── openssl.cnf
├── private
│   └── ca.key.pem
├── serial
└── serial.old