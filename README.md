### Packet Analyzer Tool with Tkinter GUI

This Python script implements a **Network Packet Analyzer** with a graphical user interface (GUI) built using `tkinter`. It captures network packets using the `scapy` library and displays key details like source and destination IP, protocol, and payload.

---

### **Features**
1. **Real-time Packet Capture**:
   - Captures and displays packets on the network in real-time.
   - Shows source and destination IP addresses, protocol type (TCP, UDP, ICMP, etc.), and a snippet of the payload.
   
2. **Intuitive GUI**:
   - Start and Stop buttons for controlling packet sniffing.
   - Scrolled text area for viewing captured packets with auto-scrolling.

3. **Multithreaded Sniffing**:
   - Runs packet sniffing in a separate thread to keep the GUI responsive.

---

### **Requirements**
- **Python 3.6+**
- Libraries:
  - `tkinter` (pre-installed with Python)
  - `scapy` (install using `pip install scapy`)

---

### **How to Use**
1. **Install Required Libraries**:
   Ensure `scapy` is installed:
   ```bash
   pip install scapy
   ```

2. **Run the Script**:
   ```bash
   python packet_analyzer.py
   ```

3. **Start Sniffing**:
   - Click the **"Start Sniffing"** button to begin capturing packets.
   - The captured packets will appear in the text area.

4. **Stop Sniffing**:
   - Click **"Stop Sniffing"** to halt packet capture.

---

### **GUI Components**
1. **Display Area**:
   - Shows packet information such as:
     - Source IP
     - Destination IP
     - Protocol (TCP, UDP, ICMP, etc.)
     - Truncated payload (in hex).

2. **Buttons**:
   - **Start Sniffing**: Begins packet capture.
   - **Stop Sniffing**: Stops packet capture.

3. **Thread Management**:
   - Sniffing runs in a background thread to keep the GUI interactive.

---

### **Code Highlights**
- **Packet Capture**:
  Captures packets using the `sniff` function from `scapy`. Filters packets with an `IP` layer and extracts relevant data.
  
- **Multithreading**:
  Ensures that packet sniffing does not freeze the GUI by running in a separate thread.

- **Stop Filter**:
  Stops sniffing gracefully when the "Stop" button is clicked.

---

### **Future Enhancements**
- Add protocol-specific decoding for detailed insights.
- Allow filtering by IP, protocol, or port.
- Save captured packets to a file in formats like PCAP.

---

### **Disclaimer**
This tool is for **educational purposes only**. Unauthorized packet capture may violate privacy laws. Ensure you have explicit permission to analyze network traffic.
