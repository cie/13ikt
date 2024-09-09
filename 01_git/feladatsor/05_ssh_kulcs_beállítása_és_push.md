# ssh kulcs beállítása

A GitHubon HTTPS vagy SSH protokollon lehet autentikálni. Ebben a feladatban az SSH protokollt fogjuk használni.

Ehhez szükségünk lesz egy SSH kulcspárra. Az egyik része a privát kulcs, amit soha ne ossz meg senkivel, a másik része a publikus kulcs, amit a GitHubon be tudsz állítani, hogy a GitHub azonosítani tudja a gépedet.

Készíts el egy új ssh kulcspárt az alábbi paranccsal:

```bash
ssh-keygen
```

Ez meg fog kérdezni egy helyet, ahova elmentheti a kulcsot, de felajánl valamit, azt fogadd el az Enter gommbal:

```
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/user/.ssh/id_ed25519):   <itt nyomj Entert>
```

Azután megkérdezi, hogy jelszót (passphrase-t) szeretnél-e a kulcshoz. Ez védi a privátk kulcsot, ha esetleg ellopnák. Ha nem szeretnél, akkor hagyd üresen. Ha mások által hozzáférhető gépen vagy, akkor viszont mindenképp adj meg jelszót, hogy ne lehessen használni a kulcsodat a jelszó nélkül. Ha beírsz egy jelszót, lehet, hogy nem fogsz látni gépelés közben semmit, de ez linuxon így szokás.

```
Enter passphrase (empty for no passphrase):   <jelszó>
Enter same passphrase again:   <jelszó>
```

Ezután kiírja, hogy hova mentette a privát és a publikus kulcsot:

```
Your identification has been saved in /home/user/.ssh/id_ed25519.
Your public key has been saved in /home/user/.ssh/id_ed25519.pub.
```

Ezek közül a publikus kulcsra lesz szükségünk. Írassuk ki a tartalmát a `cat` paranccsal:

```bash
cat ~/.ssh/id_ed25519.pub
```

A `~` linuxon a home könyvtárat jelenti, pl. `/home/user`.

Ezt a sort másold ki, és add hozzá a GitHub fiókodhoz a következő útvonalon: GitHub -> jobb felső user menü -> Settings (középtájt) -> SSH and GPG keys (bal oldalt középtájt) -> New SSH key (jobb felső sarok).

---

A kulcs hozzáadása után próbáld ki, hogy működik-e:

```bash
git push -u origin main
```

(A `-u` csak az első pusholáskor kell, és azt jelezi, hogy ezt a távoli repót szeretnéd beállítani alapértelmezettnek a `main` ág esetén. Ha ezután simán `git push`-t adsz ki a `main` ágon, akkor nem kell megadni a távoli repót.)
