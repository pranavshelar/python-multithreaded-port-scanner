# python-multithreaded-port-scanner
🛡️ Multithreaded Port Scanner (Python)

A high-performance multithreaded TCP port scanner built using Python, socket programming, and a queue-based worker model.
Designed to efficiently scan large port ranges with proper synchronization and clean architecture.

📌 Features

⚡ Multithreaded scanning using worker threads

🔒 Thread-safe port distribution using queue.Queue

🌐 TCP connect scan (connect_ex)

🧠 Banner grabbing for service identification

⏱️ Timeout handling for faster scans

📝 Scan results saved to a log file

🧹 Clean, modular, and readable code

💻 Cross-platform (Windows / Linux)

🧠 How It Works (Architecture)

All target ports are added to a thread-safe queue

Multiple worker threads pull ports from the queue

Each thread attempts a TCP connection

If a port is open:

The service banner is captured

Results are printed and logged

Threads exit gracefully when the queue is empty

This design avoids race conditions and scales efficiently.

🚀 Usage
Clone the repository
git clone https://github.com/your-username/python-multithreaded-port-scanner.git
cd python-multithreaded-port-scanner

Run the scanner
python port_scanner.py

Example Input
Enter Target IP: 127.0.0.1
Start Port: 1
End Port: 1024

📂 Sample Output
[+] Port 22 OPEN   | Banner: SSH-2.0-OpenSSH_8.9
[+] Port 80 OPEN   | Banner: HTTP/1.1 200 OK


Results are also saved in:

scan_results.txt

🧩 Technologies Used

Python 3

socket

threading

queue

TCP/IP networking

⚠️ Legal Disclaimer

This tool is intended for educational purposes only.
Scan only systems you own or have explicit permission to test.
The author is not responsible for misuse.
