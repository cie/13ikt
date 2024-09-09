# Git add

Git-ben kommitolás két lépésből áll: először előkészítjük a kommitolandó fájlokat a `git add` paranccsal egy külön területre. Ennek a területnek kb hat neve is van:

- staging area
- staged changes
- cache
- index
- changes to be committed
- cached

de ugyanarról van szó: egy előkészítési terület a kommitolandó változtatásoknak. Ezután pedig a `git commit` paranccsal kommitolunk.

A `git add` parancs a következőképpen használható:

```bash
git add <fájlnév>
```

vagy ha az összes módosítást elő akarod készíteni kommitolásra:

```bash
git add -A
```

Adj hozzá egy fájlt a `git add` paranccsal.

A `git status` parancs kiírja, hogy mi van előkészítve. Próbáld ki! Ilyesmit ír ki:

```
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   hello.js
```

Azután a `git add -A` paranccsal add hozzá az összes fájlt. Nézd meg újra a `git status` paranccsal.

Ahogy a `git status` kimenete írja, ki is lehet venni a staging areából egy fájlt a `git rm --cached <fájlnév>` paranccsal (hopp, itt már cached-nek hívják!).

Próbáld ki, hogy kiveszel az említett paranccsal egy fájlt, és megnézed a `git status` kimenetét! Aztán tedd vissza!

VSCode-ban bal oldalt általában a harmadik ikon a Source Control, ahol tudod menedzselni a git repót. Itt is tudsz addolni a + gombokkal egy fájlt vagy az összeset, és visszavenni a staging areából a mínusz gombokkal egy fájlt vagy az összeset.
