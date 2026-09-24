# Šolski IS – podpora šolskemu delu na daljavo

Projekt pri predmetu RPS – Računalniški produkti in storitve.

## Skupina
| Član | Vloga |
|------|-------|
| Jernej Robnik | Vzdrževalec IS |
| Vid Strmčnik | Razvijalec |
| Lan Plazar | Razvijalec |

Mentor: Andraž Pušnik

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
| Administrator | vid.strmcnik.20654@dijak.sc-celje.si | admin123 |
| Učitelj | andraz.pusnik@sc-celje.si | geslo123 |
| Učenec | dijak@dijak.sc-celje.si | geslo123 |

Aplikacija: http://localhost:8080. Pred javno objavo zamenjajte vsa testna gesla.
