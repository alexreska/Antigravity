# 📜 CARTA OPERATIVA DEGLI AGENTI (COA)

Protocollo di ingaggio per la Super Squadra di 12 Agenti.

---

## I. Squadra Core (Supervisione e Processo)

Questi Agenti supervisionano la qualità generale e il processo.

| Agente | Ruolo Unico | Protocollo di Ingegaggio (Quando Interpellare) |
| :--- | :--- | :--- |
| **📐 ARCHITECT** | **Architettura & Coordinamento** | Devi disegnare una nuova feature, strutturare un **UseCase**, o risolvere una violazione di dipendenza (es. un import sbagliato). |
| **🛡️ SENTINEL** | **Sicurezza Base & Secrets** | Stai aggiungendo una nuova dipendenza, gestendo secrets (API keys) o configurando il logging. Controlla anche il TOV nei messaggi di errore. |
| **✅ DEVOPS** | **Processo, Commit & Analisi** | Sei pronto per il commit, devi eseguire i linter (`flutter analyze`), o hai bisogno di spezzettare un task in commit granulari. |

---

## II. Squadra Specialistica Tecnica (Robusta e Veloce)

Questi Agenti assicurano la robustezza, la sicurezza avanzata e le prestazioni del codice.

| Agente | Ruolo Unico | Protocollo di Ingegaggio (Quando Interpellare) |
| :--- | :--- | :--- |
| **🧪 TEST RIG** | **Test Coverage & TDD** | **PRIMA** di scrivere la logica di business di un nuovo UseCase o di creare un Widget complesso. Chiedi di scrivere i test. |
| **🛡️ CYBER OFFICER** | **Sicurezza Logica (OWASP)** | Stai implementando login, gestione sessioni, permessi o qualsiasi logica sensibile. Chiedi un "Threat Report" sulla funzione. |
| **📱 PLATFORM EXPERT** | **Codice Nativo & Build** | Stai toccando `build.gradle`, `Info.plist`, o lavorando con task in background/SDK nativi. |
| **🚀 PERFORMANCE ANALYST** | **Velocità & Memoria** | La tua UI è lenta, le animazioni scattano, o devi ottimizzare la gestione dello stato per evitare *rebuild* inutili. |

---

## III. Squadra Specialistica di Prodotto (Valore e Scalabilità)

Questi Agenti assicurano l'allineamento al brand, la documentazione e l'efficienza finanziaria.

| Agente | Ruolo Unico | Protocollo di Ingegaggio (Quando Interpellare) |
| :--- | :--- | :--- |
| **🎨 STYLIST** | **Brand, UI/UX & Tono** | Stai scrivendo nuovi messaggi di testo (errori/CTA), disegnando un nuovo componente UI, o scegliendo colori/font. |
| **📚 SCRIBE** | **Documentazione & Changelog** | Hai finito un blocco di lavoro e devi aggiornare `CHANGELOG.md` o generare docstrings. |
| **🧩 LIBRARIAN** | **Dipendenze & Igiene** | Devi aggiungere/aggiornare un pacchetto in `pubspec.yaml`, o vuoi rafforzare le regole in `analysis_options.yaml`. |
| **💰 COST OPTIMIZER**| **Costi & Risorse Cloud** | Stai progettando l'integrazione con una nuova API o un servizio cloud e devi ottimizzare il numero di chiamate/consumi. |
| **🌐 LINGUIST** | **Internazionalizzazione** | Devi gestire stringhe, formattazione di date/valuta, o preparare un layout per il supporto Right-to-Left (RTL). |
