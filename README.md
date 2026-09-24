# Šolski IS – podpora šolskemu delu na daljavo

Projekt pri predmetu RPS – Računalniški produkti in storitve.

## Skupina
| Član | Vloga |
|------|-------|
| Jernej | Vzdrževalec IS |
| Vid Strmčnik | Razvijalec |
| Lan | Razvijalec |

Mentor: _ime mentorja_

## Opis
Spletna aplikacija s tremi pogledi (administrator, učitelj, učenec). Teče v Docker vsebnikih na Linux strežniku in je objavljena na javni domeni prek HTTPS.

## Struktura repozitorija
```
aplikacija/   izvorna koda spletne aplikacije
baza/         SQL skripte (shema, testni podatki)
docs/         specifikacija, ER diagram, skice, tehnična dokumentacija
porocila/     dnevna in tedenska poročila
docker-compose.yml
.env.example
```

## Zagon
```
cp .env.example .env
docker compose up -d
```

## Dokumentacija
- [Specifikacija](docs/specifikacija.md)
- [ER diagram](docs/er-diagram.md)
- [Skice (wireframe)](docs/wireframes.md)
- [Poročilo 1. teden](porocila/teden-1.md)

## Pravila dela z Gitom
- Veji: `main` (stabilna) in `develop`; delo poteka na vejah `feature/ime-funkcije`.
- Spremembe v `main` samo prek vlečnih zahtevkov (pull request) s pregledom drugega člana.
- Jasna sporočila commitov, napake v GitHub Issues.

## Prijava v testno okolje (po prvem zagonu se samodejno vnesejo testni podatki)
| Vloga | E-pošta | Geslo |
|-------|---------|-------|
| Administrator | admin@sola.si | admin123 |
| Učitelj | ucitelj1@sola.si … ucitelj20@sola.si | geslo123 |
| Učenec | ucenec1@sola.si … ucenec100@sola.si | geslo123 |

Aplikacija: http://localhost:8080. Pred javno objavo zamenjajte vsa testna gesla.
