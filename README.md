# btc_bit_checker
BTC Bit Checker – Private Key Range Scanner
# 🧠 BTC Bit Checker – Private Key Range Scanner

**Bitcoin private key range scanner** that checks compressed and uncompressed addresses (BIP44, BIP49, BIP84) against a database of known Bitcoin addresses.

> ⚠️ This tool is for educational and research purposes only. Don't use it against any wallet or system you don't own.

---

## 💡 What It Does

- Scans a range of private keys using custom bit ranges (e.g. `66–70`)
- Converts keys into **multiple address types** (Legacy, P2SH, SegWit)
- Checks if any of the addresses match those in your local SQLite address database
- Supports **multi-processing** for faster brute-force performance
- Outputs hits to `found_keys.txt` including WIF and address types
- Shows live memory usage and progress

---

## 📦 Included Files

- `btc_bit_checker.py` – the main Python script
- `addresses111.db` – your database of BTC addresses to compare against
- `found_keys.txt` – results if any match is found
- `btc_bit_checker.exe` *(optional)* – precompiled standalone Windows version
- `requirements.txt` – Python dependencies

---

## 🧪 Example Usage

### ▶️ Run with Python

```bash
pip install -r requirements.txt
python btc_bit_checker.py
Then enter the bit range to scan:
From bit: 66
To bit: 70
🪟 Run as Windows Executable

If you're using the .exe version:
Make sure the following files are in the same folder:
btc_bit_checker.exe
addresses111.db

Double-click btc_bit_checker.exe
Enter the bit range as prompted.

🧾 Output Format
If a matching address is found in the database:


💰 MATCH FOUND IN DATABASE!
🔑 Private Key: 0xABCDEF...
Compressed: ('1ABC...', '3DEF...', 'bc1...')
Uncompressed: ('1XYZ...', '3UVW...', 'bc1...')
🎁 If this address has balance, please support my work with a 10% donation!
BTC donate: bc1q4nyq7kr4nwq6zw35pg0zl0k9jmdmtmadlfvqhr
All hits are saved to found_keys.txt.

🛠 Dependencies
Install via pip:
pip install -r requirements.txt
requirements.txt
ecdsa
psutil
base58
bech32

🙏 Support
If this tool helped you recover or discover an address with a balance, consider donating to support continued development:

BTC donation address:
bc1q4nyq7kr4nwq6zw35pg0zl0k9jmdmtmadlfvqhr

📝 License
MIT License – open-source, but use responsibly. You're fully responsible for how you use this tool.
