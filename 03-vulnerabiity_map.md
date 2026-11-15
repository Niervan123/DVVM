# Vulnerability Map (OWASP IoT Top 10, 2018)

| # | Vulnerability | OWASP | Exploit | Fix |
|---|---|---|---|---|
| 1 | Hardcoded admin password | I1 | Extract from firmware or guess | Per-device hashed password |
| 2 | Dispense with no login | I2 | Call the dispense URL directly | Require auth token |
| 3 | Replayable commands | I7 | Sniff Wi-Fi, resend command | TLS plus one-time nonces |
| 4 | Open debug port | I10 | USB-UART cable gives a shell | Disable or lock console |
| 5 | Fake firmware update (stretch) | I4 | Upload modified firmware | Signed firmware |
