# git init

A következő feladatokban egy olyan mappában dolgozz, amiben még nincs git repó.

Hozz létre egy új git repót a mappában a `git init` paranccsal, úgy, hogy `main` legyen a fő ág.

Lehet, hogy kiír egy figyelmeztetést, hogy nincs beállítva, hogy `master` vagy `main` legyen a fő ág:

```
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint:   git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint:   git branch -m <name>
```

Korábban `master` volt az alapbeállítás, de egy ideje `main`-re változtatták. Ha még nem lett beállítva ez a gépen, akkor a következő paranccsal lehet beállítani:

```bash
git config --global init.defaultBranch main
```

Ha viszont már létrehoztad `master` fő ággal, akkor a következő paranccsal tudod átnevezni (amit a figyelmeztetésben is ír):

```bash
git branch -m main
```

Ha elrontottál valamit és törölni szeretnéd a repót, akkor a következő paranccsal tudod:

```bash
rm -rf .git
```
