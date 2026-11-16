# 67_Blood-Bank_RU-26-02068_1C_Tanshika-sinha
# 🩸 Blood Bank Management System

A simple, menu-driven command-line application written in Python to manage a blood bank. It lets you register donors, issue blood units, view current stock, and search donors by blood group.

> **Project No. 67**

---

## ✨ Features

- **Add Donor** – Save donor name, blood group, and units donated to `donors.txt`, and automatically update stock.
- **Issue Blood** – Issue units of a blood group, with a check for insufficient stock.
- **View Stock** – Display available units for all 8 blood groups.
- **Search Donors** – List all donors of a given blood group with the total count.
- **Input Validation** – Handles invalid blood groups, non-numeric / zero / negative units, empty names, and names containing commas.

---

## 🛠️ Requirements

- Python 3.6 or higher
- No external libraries needed (uses only the built-in `os` module)

---

## 🚀 Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/<your-username>/blood-bank-management-system.git
   cd blood-bank-management-system
   ```

2. **Run the program**

   ```bash
   python blood_bank.py
   ```

   > Replace `blood_bank.py` with the actual name of your script file.

---

## 📋 Usage

When you run the program, you will see this menu:

```
================================
     BLOOD BANK MANAGEMENT
================================
1. Add donor
2. Issue blood
3. View stock
4. Search donors
5. Exit
================================
```

| Option | Description |
|--------|-------------|
| 1 | Enter donor name, blood group, and units to add a donor and increase stock |
| 2 | Enter blood group and units to issue blood from stock |
| 3 | View available stock of all blood groups |
| 4 | Enter a blood group to list matching donors |
| 5 | Exit the program |

### Valid Blood Groups

`A+`, `A-`, `B+`, `B-`, `AB+`, `AB-`, `O+`, `O-`

---

## 💡 Sample Run

```
Enter your choice: 1
Enter donor name: Rahul Sharma
Enter blood group: a+
Enter units: 3
Donor saved to donors.txt. Stock of A+ is now 13 units.

Enter your choice: 2
Enter blood group: O-
Enter units: 2
Insufficient stock: only 0 unit(s) of O- available.
```

---

## 📁 Data Storage

Donor records are stored in `donors.txt` in this format:

```
Name, Blood Group, Units
```

On first run, the file is created with two sample records:

```
Meena Joshi, O+, 1
Suresh Rao, O+, 2
```

---

## 🧱 Project Structure

```
blood-bank-management-system/
├── blood_bank.py    # Main program
├── donors.txt       # Donor records (auto-created on first run)
└── README.md
```

---

## ⚠️ Known Limitations

- Blood stock is held **in memory** and resets to the initial values every time the program restarts. Only donor records persist in `donors.txt`.
- Donor names cannot contain commas (since the file is comma-separated).
- Issuing blood does not record who received it.

---

## 🔮 Future Improvements

- Persist blood stock in a file or database
- Track issued-blood history
- Add blood-group compatibility checks (e.g., O- as universal donor)
- Add donation dates and donor contact details
- Build a GUI or web interface

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to fork the repo and open a pull request.

---

