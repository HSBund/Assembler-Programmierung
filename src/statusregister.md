# Flags im Statusregister

## Information

- Material für Vorlesungsreihe Assembler-Programmierung an der HS Bund
- Aktuellste Version: https://github.com/HSBund/Assembler-Programmierung

## Status Register (SREG) – Bitbelegung

| Bit | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|:---:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Flag | I | T | H | S | V | N | Z | C |

## Status Register (SREG) – Flags

| Flag | Bedeutung | Kurze Erklärung |
|:----:|-----------|-----------------|
| **I** | Global Interrupt Enable | Aktiviert (`1`) bzw. deaktiviert (`0`) globale Interrupts. |
| **T** | Bit Copy Storage | Temporäres Bit für Bit-Kopierbefehle (`BST`, `BLD`). |
| **H** | Half Carry | Zeigt einen Übertrag zwischen Bit 3 und Bit 4 an (wichtig bei BCD-Arithmetik). |
| **S** | Sign Flag | Vorzeichenflag; berechnet als `N ⊕ V` (XOR von N und V). |
| **V** | Two's Complement Overflow | Zeigt einen Überlauf bei vorzeichenbehafteten Berechnungen an. |
| **N** | Negative Flag | Entspricht dem höchstwertigen Bit (Bit 7) des Ergebnisses. |
| **Z** | Zero Flag | Wird gesetzt, wenn das Ergebnis einer Operation `0` ist. |
| **C** | Carry Flag | Zeigt einen Übertrag (Addition) oder Borrow (Subtraktion) an. |
