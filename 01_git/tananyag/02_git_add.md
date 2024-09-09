# git add

A `git add` paranccsal tudunk fájlokat előkészíteni kommitolásra. Az előkészítési terület neve

- staged changes
- cache
- index

és még néhány, de ugyanarról van szó.

A `git add` parancs a következőképpen használható:

```bash
git add <fájlnév>
```

vagy ha az összes módosítást elő akarod készíteni kommitolásra:

```bash
git add -A
```

A `git status` parancs kiírja, hogy mi van előkészítve, és ad segítséget ahhoz, hogy kivegyél módosításokat az előkészítési területről.
