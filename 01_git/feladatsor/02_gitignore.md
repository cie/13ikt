# gitignore

A `.gitignore` fájlban megadhatjuk, hogy mely fájlokat és mappákat ne vegye figyelembe a git, amikor új fájlokat jelez.

Például az npm csomagkezelő a `node_modules` mappában tárolja a telepített csomagokat. Ezeket a fájlokat nem szeretnénk feltölteni a repóba. Ha van `node_modules` mappád és még nincs `.gitignore` fájlod, akkor a

```bash
git status
```

parancs kiírja, hogy a `node_modules` mappa nincs hozzáadva a repóhoz, ill. VSCode-ban nagyon sok új fájlt fogsz látni, amiket alapesetben hozzáadna a git a repóhoz.

Vegyél fel egy `.gitignore` fájlt a repódba, és írd bele a következőket:

```plaintext
node_modules
```

Ezután a `git status` parancs már nem fogja kiírni a `node_modules` mappát új fájlként. Viszont a `.gitingore` fájlt most már igen.
