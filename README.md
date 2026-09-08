Chat Network Application

A simple two-way command-line chat program in C using UDP sockets.

Files
chat.c — main program
udp3.c / udp3.h — UDP socket library (open/close ports, send/receive)
kbhit.c / kbhit.h — non-blocking keyboard input detection
Compiling
bash
gcc -std=gnu11 -Wall -o chat chat.c udp3.c kbhit.c
Usage

Run on both machines, each pointing at the other's IP:

bash
./chat IPV4_ADDRESS

Sent messages appear on the left, received messages on the right. Type a message starting with QUIT to exit.

Notes
Listens and sends on port 5000 (change Local_Port1 / Remote_Port1 in chat.c if needed)
One-to-one chat only, no encryption, UDP doesn't guarantee delivery
Max message length: 100 characters
