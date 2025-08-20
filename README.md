# Hamming SEC-DED Encoding and Error Correction Simulator

This project is a **Python Tkinter GUI application** that performs encoding and error detection/correction of binary data using the **Hamming SEC-DED (Single Error Correction - Double Error Detection)** algorithm.

---

## 🚀 Features

- ✅ Accepts binary input of lengths: **4, 8, 16, 32, 64 bits**  
- ✅ Generates the Hamming code (with parity bits)  
- ✅ Allows error simulation by flipping a specific bit position  
- ✅ Detects errors and shows the **syndrome** (error position)  
- ✅ Corrects single-bit errors automatically  
- ✅ Built with **Python + Tkinter GUI**  

---

## 📸 Screenshots

![App Screenshot](https://github.com/user-attachments/assets/5b683778-4361-4866-b9e9-1e1968b85431)

---

## 🖥️ How to Use

1. Select the **data length** (4, 8, 16, 32, or 64 bits).  
2. Enter your **binary data**.  
3. Click **"Generate Hamming Code"** to encode the input.  
4. (Optional) Inject an error by entering a bit position (e.g., `1` = rightmost bit).  
5. The program will:  
   - Detect the error (if any)  
   - Show the syndrome (bit position)  
   - Correct the error and display the fixed code  

---

## 📽️ Demo Video

▶️ Watch the demo video on YouTube:  
[👉 Hamming SEC-DED Demo](https://www.youtube.com/watch?v=rHKQKSCRnW0)
