<img width="1696" height="608" alt="Gemini_Generated_Image_ma2awwma2awwma2a" src="https://github.com/user-attachments/assets/e16cca59-9fb9-4913-919f-b6727cbdd8ad" />


## 🚀 Step-by-Step Implementation

### 1. 🛠️ Environment Setup
First, we update the system and install the forensic toolkit:
* **Steghide**: To hide data.
* **Stegseek**: To crack passwords.
* **Bat**: For colorful terminal output.

```bash
sudo apt update && sudo apt install steghide stegseek bat -y
2. 💉 The Injection (Embedding Data)
In this phase, we create a secret text file and embed it into a standard JPEG image using a password.

Bash
# Create the secret message
echo "CONFIRMED TARGET: Coordinates -16.6033, -49.2665" > secret.txt

# Embed the secret into the carrier image
steghide embed -cf carrier.jpg -ef secret.txt -p 123456
3. 🔍 The Forensic Attack (Cracking)
We simulate a forensic investigation where the password is unknown. We use Stegseek with a dictionary attack (rockyou.txt) to recover the secret.

Bash
stegseek carrier.jpg /usr/share/wordlists/rockyou.txt
4. 📄 Evidence Display (Final Report)
After successfully cracking the protection, we display the recovered evidence using a formatted and colorful output.

Bash
batcat --style=full --color=always carrier.jpg.out
🧠 Forensic Insights
[!IMPORTANT]
Data Persistence: Even if a file is hidden, its bit-patterns leave traces that forensic tools can detect.

Password Strength: Simple passwords (like 123456) offer zero protection against modern brute-force tools.

Integrity: Digital forensics is about uncovering the truth hidden in plain sight.

🖼️ Proof of Concept
⚠️ Disclaimer
This project is for educational purposes only. All techniques were performed in a controlled environment for cybersecurity research.
```
<img width="2810" height="1205" alt="Screenshot1" src="https://github.com/user-attachments/assets/bad64dca-e361-4ee7-95bb-89da8ad2226a" />

