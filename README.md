# 🐺 WolfBot

**Veloce. Stabile. Affidabile. Il tuo server, sotto controllo.**

WolfBot è un bot per le community di [Root](https://www.rootapp.com) che ti aiuta a gestire il server: messaggi di benvenuto, ruoli automatici, ruoli a reazione, annunci, moderazione della chat e permessi per ogni comando.

---

## ✨ Funzioni

| Funzione | Cosa fa |
|---|---|
| 👋 **Benvenuto** | Saluta i nuovi membri con un messaggio personalizzabile |
| 🎭 **Autorole** | Assegna automaticamente un ruolo a chi entra |
| 😀 **Ruoli a reazione** | Il membro clicca una reazione (anche emoji custom) e riceve il ruolo; se la toglie, il ruolo viene rimosso |
| 📢 **Annunci** | Pubblica annunci in un canale dedicato |
| 🐢 **Slow mode** | Limita la frequenza dei messaggi in un canale |
| 🧹 **Clear chat** | Cancella gli ultimi messaggi (fino a 100) o l'intera chat |
| 🔐 **Permessi per comando** | Decidi quali ruoli possono usare ogni comando |

---

## 🚀 Installazione

1. Apri la tua community su Root (versione desktop).
2. Fai clic destro su un gruppo di canali (o sul **+**), poi **Choose app**.
3. Cerca **WolfBot** nell'App Store e installalo (serve il permesso *Manage Apps*).
4. Accetta i permessi richiesti e scegli i canali in cui il bot può operare.
5. Crea nella community un ruolo chiamato **MASTER-BOSS** e assegnalo a chi deve gestire il bot.
6. Scrivi `!help` in un canale per vedere i comandi.

> Per impostazione predefinita **tutti i comandi sono riservati al ruolo `MASTER-BOSS`**.

---

## 💬 Comandi

| Comando | Descrizione |
|---|---|
| `!help` | Mostra l'elenco dei comandi |
| `!setwelcome <testo>` | Imposta il messaggio di benvenuto. Segnaposto: `{user}`, `{community}` |
| `!setwelcomechannel` | Usa il canale corrente per i benvenuti |
| `!welcometest` | Prova il messaggio di benvenuto |
| `!autorole <ruolo\|off>` | Ruolo dato ai nuovi membri |
| `!setannunci` | Usa il canale corrente per gli annunci |
| `!annuncio <testo>` | Pubblica un annuncio |
| `!rr <titolo> \| :emoji: Ruolo \| :emoji: Ruolo` | Crea un messaggio con ruoli a reazione |
| `!slowmode <secondi\|off>` | Attiva o disattiva la slow mode nel canale |
| `!clear <numero\|all>` | Cancella gli ultimi messaggi (max 100) o tutti |
| `!perm <comando> <ruolo1,ruolo2\|all\|reset>` | Decide chi può usare un comando |

### Esempi

```
!setwelcome Ciao {user}, benvenuto in {community}! 🎉
!rr Scegli i tuoi giochi | :video_game: Minecraft | :gun: Valorant | :fire: Fortnite
!slowmode 10
!clear 5
!perm annuncio Moderatore,MASTER-BOSS
```

I ruoli usati nei ruoli a reazione devono già esistere nella community, con lo stesso nome.

---

## 🔑 Permessi richiesti

| Permesso | Perché serve |
|---|---|
| `manageRoles` (community) | Assegnare e togliere ruoli (autorole, ruoli a reazione) |
| `createMessage` (canale) | Rispondere ai comandi e inviare benvenuti e annunci |
| `deleteMessageOther` (canale) | Slow mode e clear chat |
| `createMessageReaction` (canale) | Aggiungere le reazioni ai messaggi dei ruoli a reazione |
| `viewMessageHistory` (canale) | Leggere i messaggi da cancellare con `!clear` |

Il bot può assegnare solo ruoli i cui permessi non superano i suoi.

---

## 🔒 Privacy

Leggi la [Privacy Policy](PRIVACY.md).

## 🆘 Supporto

Hai trovato un problema o vuoi una nuova funzione? Apri una *issue* in questo repository.

---

*WolfBot è un progetto indipendente e non è affiliato a Root.*
