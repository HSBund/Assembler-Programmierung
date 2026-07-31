# AVR-Befehle

## Information

- Material für Vorlesungsreihe Assembler-Programmierung an der HS Bund
- Aktuellste Version: https://github.com/HSBund/Assembler-Programmierung
- Fehler/Verbesserungen/Ideen: https://github.com/HSBund/Assembler-Programmierung/issues



| Mnemonik | Ausgeschrieben | Beschreibung | Operanden / Register | Geänderte SREG-Flags |
|----------|----------------|--------------|----------------------|----------------------|
| `ADD` | Add without Carry | Addiert zwei Register und speichert das Ergebnis im Zielregister. | `Rd, Rr` (`R0–R31`) | `H`, `V`, `N`, `Z`, `C`, `S` |
| `ADIW` | Add Immediate to Word | Addiert eine Konstante zu einem 16-Bit-Registerpaar. | `R25:R24`, `R27:R26`, `R29:R28`, `R31:R30`; Konstante `0–63` | `V`, `N`, `Z`, `C`, `S` |
| `AND` | Logical AND | Bitweises UND zweier Register. | `Rd, Rr` (`R0–R31`) | `V`, `N`, `Z`, `S` |
| `ANDI` | AND with Immediate | Bitweises UND eines Registers mit einer Konstante. | `R16–R31`; Konstante `0–255` | `V`, `N`, `Z`, `S` |
| `BREQ` | Branch if Equal | Springt relativ, wenn das Zero-Flag gesetzt ist. | Relatives Sprungziel | – |
| `BRLO` | Branch if Lower | Springt, wenn das Carry-Flag gesetzt ist (Unsigned `<`). | Relatives Sprungziel | – |
| `BRNE` | Branch if Not Equal | Springt, wenn das Zero-Flag gelöscht ist. | Relatives Sprungziel | – |
| `BRSH` | Branch if Same or Higher | Springt, wenn das Carry-Flag gelöscht ist (Unsigned `>=`). | Relatives Sprungziel | – |
| `CP` | Compare | Vergleicht zwei Register (Subtraktion ohne Speichern). | `Rd, Rr` (`R0–R31`) | `H`, `V`, `N`, `Z`, `C`, `S` |
| `CPI` | Compare with Immediate | Vergleicht Register mit einer Konstante. | `R16–R31`; Konstante `0–255` | `H`, `V`, `N`, `Z`, `C`, `S` |
| `DEC` | Decrement | Verringert den Registerinhalt um 1. | `R0–R31` | `V`, `N`, `Z`, `S` |
| `EOR` | Exclusive OR | Bitweises exklusives ODER zweier Register. | `Rd, Rr` (`R0–R31`) | `V`, `N`, `Z`, `S` |
| `IN` | Load from I/O Space | Liest ein I/O-Register in ein Register. | `Rd` (`R0–R31`), I/O-Adresse | – |
| `INC` | Increment | Erhöht den Registerinhalt um 1. | `R0–R31` | `V`, `N`, `Z`, `S` |
| `LD` | Load Indirect | Lädt ein Byte aus dem SRAM über `X`, `Y` oder `Z`. | `Rd` (`R0–R31`), `X`, `Y`, `Z`, `X+`, `-X`, `Y+`, `-Y`, `Z+`, `-Z` | – |
| `LDD` | Load Indirect with Displacement | Lädt ein Byte aus dem SRAM über `Y+q` oder `Z+q`. | `Rd` (`R0–R31`), `Y+q`, `Z+q` | – |
| `LDI` | Load Immediate | Lädt eine Konstante in ein Register. | `R16–R31`; Konstante `0–255` | – |
| `LSL` | Logical Shift Left | Verschiebt alle Bits um eine Stelle nach links. | `R0–R31` | `H`, `V`, `N`, `Z`, `C`, `S` |
| `LSR` | Logical Shift Right | Verschiebt alle Bits um eine Stelle nach rechts. | `R0–R31` | `V`, `N`, `Z`, `C`, `S` |
| `MOV` | Move Register | Kopiert den Inhalt eines Registers in ein anderes. | `Rd, Rr` (`R0–R31`) | – |
| `OUT` | Store to I/O Space | Schreibt den Inhalt eines Registers in ein I/O-Register. | I/O-Adresse, `R0–R31` | – |
| `OR` | Logical OR | Bitweises ODER zweier Register. | `Rd, Rr` (`R0–R31`) | `V`, `N`, `Z`, `S` |
| `ORI` | OR with Immediate | Bitweises ODER eines Registers mit einer Konstante. | `R16–R31`; Konstante `0–255` | `V`, `N`, `Z`, `S` |
| `POP` | Pop from Stack | Holt das oberste Byte vom Stack in ein Register. | `R0–R31` | – |
| `PUSH` | Push onto Stack | Legt den Registerinhalt auf den Stack. | `R0–R31` | – |
| `RCALL` | Relative Call to Subroutine | Ruft ein Unterprogramm relativ auf und speichert die Rücksprungadresse auf dem Stack. | Relatives Sprungziel | – |
| `RET` | Return from Subroutine | Holt die Rücksprungadresse vom Stack und kehrt zum Aufrufer zurück. | – | – |
| `RJMP` | Relative Jump | Springt relativ zu einer Zieladresse. | Relatives Sprungziel | – |
| `SBIC` | Skip if Bit in I/O Register Cleared | Überspringt den nächsten Befehl, wenn ein I/O-Bit `0` ist. | I/O-Adresse, Bit `0–7` | – |
| `SBIS` | Skip if Bit in I/O Register Set | Überspringt den nächsten Befehl, wenn ein I/O-Bit `1` ist. | I/O-Adresse, Bit `0–7` | – |
