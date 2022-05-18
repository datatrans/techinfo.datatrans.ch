# Supported Ciphers

We will phase out deprecated ciphers in two steps. We are constantly monitoring cipher usage and contact merchants individually if we see affected ciphers in active usage. Nevertheless, we kindly ask you to test your application for proper support of the used cipher suites.

### **Dates**

#### **Phase 1**

Phase 1 will be implemented with the announced certificate renewal.

**Test Environment: 14.06.2022**\
pay.sandbox.datatrans.com\
admin.sandbox.datatrans.com\
api.sandbox.datatrans.com\
\
**Productive environment: 12.07.2022**\
pay.datatrans.com\
admin.datatrans.com\
api.datatrans.com

#### Phase 2

Phase 2 follows after reviewing the change in usage of the phase 1 cipher selection.

**Test Environment: 09.08.2022**\
pay.sandbox.datatrans.com\
admin.sandbox.datatrans.com\
api.sandbox.datatrans.com\
\
**Productive environment: 06.09.2022**\
pay.datatrans.com\
admin.datatrans.com\
api.datatrans.com

### **Cipher Suites**

In phase 1, we disable weak cipher block chaining (CBC) mode ciphers due to timing vulnerabilities. Additional reading: [https://docs.microsoft.com/en-us/dotnet/standard/security/vulnerabilities-cbc-mode](https://docs.microsoft.com/en-us/dotnet/standard/security/vulnerabilities-cbc-mode)

In phase 2, we continue deprecating ciphers containing Diffie-Hellman key exchange (DHE). While not considered weak when used with a 2048 bit strong key, they are very resource intensive and phased out in favour of Elliptic-curve Diffie–Hellman (ECDH).&#x20;



| Current                                                      | Phase 1                                                      | Phase 2                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| TLS\_AES\_256\_GCM\_SHA384 (`0x1302`)                        | TLS\_AES\_256\_GCM\_SHA384 (`0x1302`)                        | S\_AES\_256\_GCM\_SHA384 (`0x1302`)                          |
| TLS\_AES\_128\_GCM\_SHA256 (`0x1301`)                        | TLTLS\_AES\_128\_GCM\_SHA256 (`0x1301`)                      | TLS\_AES\_128\_GCM\_SHA256 (`0x1301`)                        |
| TLS\_CHACHA20\_POLY1305\_SHA256 (`0x1303`)                   | TLS\_CHACHA20\_POLY1305\_SHA256 (`0x1303`)                   | LS\_CHACHA20\_POLY1305\_SHA256 (`0x1303`)                    |
| TLS\_ECDHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384 (`0xc030`)      | TLS\_ECDHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384 (`0xc030`)      | TLS\_ECDHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384 (`0xc030`)      |
| TLS\_ECDHE\_RSA\_WITH\_AES\_128\_GCM\_SHA256 (`0xc02f`)      | TLS\_ECDHE\_RSA\_WITH\_AES\_128\_GCM\_SHA256 (`0xc02f`)      | TLS\_ECDHE\_RSA\_WITH\_AES\_128\_GCM\_SHA256 (`0xc02f`)      |
| TLS\_ECDHE\_RSA\_WITH\_CHACHA20\_POLY1305\_SHA256 (`0xcca8`) | TLS\_ECDHE\_RSA\_WITH\_CHACHA20\_POLY1305\_SHA256 (`0xcca8`) | TLS\_ECDHE\_RSA\_WITH\_CHACHA20\_POLY1305\_SHA256 (`0xcca8`) |
| TLS\_DHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384 (`0x9f`)          | TLS\_DHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384 (`0x9f`)          | -                                                            |
| TLS\_DHE\_RSA\_WITH\_AES\_128\_GCM\_SHA256 (`0x9e`)          | LS\_DHE\_RSA\_WITH\_AES\_128\_GCM\_SHA256 (`0x9e`)           | -                                                            |
| TLS\_DHE\_RSA\_WITH\_AES\_256\_CBC\_SHA256 (`0x6b`)          | -                                                            | -                                                            |
| TLS\_DHE\_RSA\_WITH\_AES\_128\_CBC\_SHA256 (`0x67`)          | -                                                            | -                                                            |
| TLS\_ECDHE\_RSA\_WITH\_AES\_256\_CBC\_SHA384 (`0xc028`)      | -                                                            | -                                                            |
| TLS\_ECDHE\_RSA\_WITH\_AES\_256\_CBC\_SHA (`0xc014`)         | -                                                            | -                                                            |
| TLS\_ECDHE\_RSA\_WITH\_AES\_128\_CBC\_SHA256 (`0xc027`)      | -                                                            | -                                                            |
| TLS\_ECDHE\_RSA\_WITH\_AES\_128\_CBC\_SHA (`0xc013`)         | -                                                            | -                                                            |

