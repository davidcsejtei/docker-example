# Docker és Docker compose példa

Ez egy egyszerű példa, ami egy 2 komponensből álló alkalmazás dokkerizációját mutatja be.
Két komponens:
- UI (Vue.js)
- API (Node.js + Express)

Mindkét projektben van saját Dockerfile.

Van egy közös docker-compose fájl, ami miatt a projekt gyökerében állva az egész alkalmazás elindítható dokkerben az alábbi parancs segítségével:
```
docker compose up -d
```

Ez elindít 2 container-t, amik "látják egymást".

Sikeres indítást követően a UI elérhető:
```
http://localhost:80
```
