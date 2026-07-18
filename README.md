<div align="center">

# 🇵🇱 Polski VPN — macOS

**Prosty, szybki klient VPN dla macOS (Apple Silicon) — protokół OpenVPN, pełny tunel, zero konfiguracji.**

![Platform](https://img.shields.io/badge/platform-macOS%2013%2B%20(Apple%20Silicon)-000000?logo=apple&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-3.44-02569B?logo=flutter&logoColor=white)
![Protocol](https://img.shields.io/badge/VPN-OpenVPN-blue)
![Version](https://img.shields.io/badge/version-2.0.1-success)

<a href="../../releases/latest">
  <img alt="Pobierz .dmg"
       src="https://img.shields.io/badge/⬇%20Pobierz-PolskiVPN--arm64.dmg-000000?style=for-the-badge&logo=apple">
</a>

</div>

---

## ✨ W skrócie

**Polski VPN dla macOS** to desktopowy klient VPN dla Maków z procesorem **Apple Silicon (M1 i nowsze)**. Łączy się z serwerami usługi <a href="https://polski-vpn.pl/">*Polski-VPN.pl*</a> przez protokół **OpenVPN**. Interfejs jest po polsku i minimalistyczny - wybierz serwer, wpisz dane dostępowe otrzymane po zakupie usługi i połącz się. Aplikacja chowa się do paska menu (menu bar) i może uruchamiać się przy starcie systemu.

---

## 👤 Dla kogo

| Odbiorca | Dlaczego |
|---|---|
| 🧑‍💻 Użytkownicy usługi **Polski VPN** | Dedykowany, lekki klient serwerów Polski VPN na Maca |
| 🍎 Użytkownicy **Maków Apple Silicon** | Natywna aplikacja (arm64) z paskiem menu i autostartem |
| 🔒 Szukający prostego klienta OpenVPN | Bez instalowania Tunnelblicka / OpenVPN Connect i ręcznego importu `.ovpn` |

---

## 🚀 Funkcje

| Funkcja | Opis | Status |
|---|---|:---:|
| Protokół OpenVPN | Wbudowany, zbundlowany silnik | ✅ |
| Lista serwerów | Wybór z poziomu aplikacji | ✅ |
| Pełny tunel | Cały ruch (`0.0.0.0/0`) tunelowany przez VPN | ✅ |
| DNS przez tunel | Serwery DNS z VPN-a (bez wycieku do ISP) | ✅ |
| Zapamiętywanie danych | Login/hasło w Pęku kluczy (Keychain) | ✅ |
| Auto-reconnect | Ponawianie przy zerwaniu połączenia | ✅ |
| Pasek menu (menu bar) | Ikona, menu (połącz / rozłącz / pokaż / zakończ), status | ✅ |
| Autostart | Uruchamianie przy logowaniu | ✅ |
| Start zminimalizowany | Uruchom schowany do paska menu | ✅ |
| Zero promptów | Po jednorazowej instalacji usługi pomocniczej - łączenie bez pytania o hasło | ✅ |

---

## 🔌 Protokoły - co dokładnie działa na macOS

| Protokół | Status na macOS | Dlaczego |
|---|:---:|---|
| **OpenVPN** | ✅ działa | Wspierany |
| **SoftEther** | ⛔ niedostępny | brak natywnego wsparcia |
| **SSTP** | ⛔ niedostępny | brak natywnego wsparcia |

---

## 📥 Instalacja

1. Pobierz **`PolskiVPN-arm64.dmg`** z zakładki [Releases](../../releases/latest).
2. Otwórz `.dmg` i przeciągnij **Polski VPN** do folderu **Aplikacje**.
3. Odblokuj przy pierwszym uruchomieniu (patrz niżej - *Nieznane źródło*).
4. Przy **pierwszym połączeniu** macOS poprosi **raz** o hasło administratora (jednorazowa instalacja usługi pomocniczej, która uruchamia VPN z prawami roota). Potem łączysz się **bez pytania o hasło**.
5. W aplikacji: wybierz **serwer**, wpisz **login i hasło** otrzymane po zakupie usługi, kliknij **POŁĄCZ**.

---

## ⚠️ „Nie można otworzyć - niezidentyfikowany deweloper" (nieznane źródło)

Aplikacja **nie jest notaryzowana przez Apple** (jest udostępniana bezpośrednio przez GitHub, bez konta Apple Developer). Dlatego macOS przy pierwszym uruchomieniu ją **zablokuje** - to normalne i bezpieczne dla aplikacji z zaufanego źródła. Odblokowujesz **raz**, na jeden z dwóch sposobów:

**Sposób A - przez Ustawienia systemowe (zalecany):**
1. Spróbuj uruchomić **Polski VPN** (dwuklik). Pojawi się komunikat, że pochodzi od „niezidentyfikowanego dewelopera".
2. Otwórz **Ustawienia systemowe → Prywatność i ochrona**.
3. Przewiń na dół - zobaczysz informację o zablokowanej aplikacji. Kliknij **„Otwórz mimo to"**.
4. Potwierdź **„Otwórz"** w kolejnym oknie (możesz potrzebować hasła/Touch ID).

**Sposób B - przez Terminal (jedna komenda):**
```bash
xattr -dr com.apple.quarantine "/Applications/polski_vpn.app"
```
Potem uruchom aplikację normalnie.

---

## 🖥️ Wymagania

| Element | Wymaganie |
|---|---|
| System | macOS 13 (Ventura) lub nowszy |
| Architektura | **Apple Silicon (arm64)** - M1, M2, M3, M4, M5… *(wersja dla Maków Intel - planowana)* |
| Uprawnienia | Jednorazowo hasło administratora (instalacja usługi pomocniczej) |
| Sieć | Dostęp do internetu + aktywne konto na [polski-vpn.pl](https://polski-vpn.pl/) |

---

## 📜 Licencje

- Kod aplikacji — własność dostawcy usługi **Polski-VPN.pl**.
- **OpenVPN** — GPLv2 (oficjalny, uruchamiany jako osobny proces).
- Biblioteki: **OpenSSL** (Apache 2.0), **LZO** (GPLv2), **LZ4** (BSD-2), **pkcs11-helper** (GPLv2/BSD).

---

<div align="center">
<sub>Zbudowane dla użytkowników Polski-VPN.pl</sub>
</div>
