# 📅 Yocto 6-Monats-Lernplan

Dieser Plan ist für **Montag bis Donnerstag** pro Woche strukturiert und deckt alle Phasen ab: Grundlagen, Yocto-Setup, SDK, Debugging, Sicherheit und Abschlussprojekt.

---

## ✅ Monat 1: Grundlagen & Setup

### Woche 1
- **Mo:** Linux-Umgebung einrichten (Ubuntu/Debian), Tools installieren (`git`, `gcc`, `make`, `python3`).
- **Di:** Yocto Quick Start Guide lesen, Begriffe verstehen (Poky, BitBake, Layers, Recipes).
- **Mi:** Poky klonen:
  ```bash
  git clone git://git.yoctoproject.org/poky.git
  cd poky
  git checkout kirkstone
  ```
  Abhängigkeiten installieren.
- **Do:** Erstes Image bauen:
  ```bash
  source oe-init-build-env
  bitbake core-image-minimal
  ```

### Woche 2
- **Mo:** `local.conf` und `bblayers.conf` analysieren, `meta-openembedded` hinzufügen.
- **Di:** Image mit neuem Layer bauen, QEMU-Test starten:
  ```bash
  runqemu qemux86-64
  ```
- **Mi:** DISTRO_FEATURES anpassen, Pakete hinzufügen (`nano`, `htop`).
- **Do:** Änderungen dokumentieren und auf GitHub hochladen.

### Woche 3
- **Mo:** Eigenen Layer erstellen:
  ```bash
  bitbake-layers create-layer meta-myproject
  ```
- **Di:** Erstes Recipe (Hello World) schreiben.
- **Mi:** Image mit eigenem Recipe bauen.
- **Do:** Test in QEMU, Dokumentation.

### Woche 4
- **Mo:** Build-Logs analysieren, `bitbake -c cleansstate` nutzen.
- **Di:** Weitere Pakete hinzufügen.
- **Mi:** Root-Filesystem anpassen.
- **Do:** Review und GitHub-Update.

---

## ✅ Monat 2: Image-Customization & Layer-Management

### Woche 5
- **Mo:** Eigenes Image-Recipe erstellen.
- **Di:** SSH-Zugang hinzufügen.
- **Mi:** Image für Raspberry Pi oder BeagleBone bauen.
- **Do:** Boot auf Hardware testen.

### Woche 6
- **Mo:** DISTRO_FEATURES erweitern.
- **Di:** Webserver hinzufügen.
- **Mi:** Image-Anpassungen dokumentieren.
- **Do:** Review und GitHub-Update.

### Woche 7
- **Mo:** Weitere Software integrieren.
- **Di:** Layer-Struktur optimieren.
- **Mi:** Test auf Hardware.
- **Do:** Dokumentation.

### Woche 8
- **Mo:** Review aller Anpassungen.
- **Di:** Vorbereitung SDK-Phase.
- **Mi:** GitHub-Update.
- **Do:** Fragen sammeln.

---

## ✅ Monat 3: SDK & Cross-Compilation

### Woche 9
- **Mo:** SDK generieren:
  ```bash
  bitbake -c populate_sdk core-image-minimal
  ```
- **Di:** SDK installieren.
- **Mi:** Erste C-App schreiben.
- **Do:** Cross-Compile und Deploy.

### Woche 10
- **Mo:** Workflow automatisieren (Makefile).
- **Di:** Weitere Apps cross-compilieren.
- **Mi:** Debugging vorbereiten.
- **Do:** Dokumentation.

### Woche 11
- **Mo:** SDK-Review.
- **Di:** GitHub-Update.
- **Mi:** Fragen klären.
- **Do:** Vorbereitung Debugging.

### Woche 12
- **Mo:** SDK-Phase abschließen.
- **Di:** Review.
- **Mi:** Dokumentation.
- **Do:** GitHub-Update.

---

## ✅ Monat 4: Debugging & Erweiterte Features

### Woche 13
- **Mo:** `devtool` nutzen.
- **Di:** Debugging mit `gdb`, `strace`.
- **Mi:** Build-Zeiten analysieren.
- **Do:** Performance optimieren.

### Woche 14
- **Mo:** Externe Toolchains testen.
- **Di:** Layer-Optimierung.
- **Mi:** Dokumentation.
- **Do:** GitHub-Update.

### Woche 15
- **Mo:** Review Debugging.
- **Di:** Performance-Check.
- **Mi:** Fragen klären.
- **Do:** Vorbereitung Security.

### Woche 16
- **Mo:** Debugging-Phase abschließen.
- **Di:** Dokumentation.
- **Mi:** GitHub-Update.
- **Do:** Vorbereitung OTA.

---

## ✅ Monat 5: Sicherheit & OTA

### Woche 17
- **Mo:** Secure Boot verstehen.
- **Di:** Image-Signierung implementieren.
- **Mi:** Test auf Hardware.
- **Do:** Dokumentation.

### Woche 18
- **Mo:** OTA-Update mit RAUC.
- **Di:** OTA-Test.
- **Mi:** Fehleranalyse.
- **Do:** GitHub-Update.

### Woche 19
- **Mo:** Sicherheits-Features dokumentieren.
- **Di:** Review.
- **Mi:** Vorbereitung Abschlussprojekt.
- **Do:** GitHub-Update.

### Woche 20
- **Mo:** Security-Phase abschließen.
- **Di:** Dokumentation.
- **Mi:** GitHub-Update.
- **Do:** Projektstart.

---

## ✅ Monat 6: Abschlussprojekt

### Woche 21–24
- **Mo:** Eigenes Layer finalisieren.
- **Di:** Custom Image + SDK integrieren.
- **Mi:** OTA-Funktion hinzufügen.
- **Do:** GitHub-Portfolio & Präsentation.

---

✅ **Tipp:** Jede Woche am Donnerstag alles dokumentieren und auf GitHub pushen.
