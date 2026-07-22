# renovate-demo

Demo repozitorij za prezentaciju automatskog ažuriranja dependencyja.

Sadrži namjerno **stare verzije** dependencyja kako bi Renovate imao što predložiti.

## Što je unutra

- `pom.xml` — Maven projekt s par zastarjelih dependencyja
- `renovate.json` — Renovate konfiguracija
- `.github/workflows/ci.yml` — GitHub Actions CI (build + testovi na svakom PR-u)

## Postavljanje Renovate bota

1. Idi na [github.com/apps/renovate](https://github.com/apps/renovate)
2. Klikni **Install**
3. Odaberi ovaj repozitorij
4. Renovate će u roku par minuta otvoriti prvi PR s konfiguracijom (ako `renovate.json` već postoji, odmah prelazi na dependency PR-ove)

## Što će Renovate napraviti

Nakon instalacije, bot će automatski otvoriti PR-ove za svaku zastarjelu verziju:

| Dependency | Trenutna verzija |
|---|---|
| spring-boot-starter | 3.1.0 |
| jackson-databind | 2.14.0 |
| guava | 31.0-jre |
| junit-jupiter | 5.9.0 |

## Lokalno pokretanje testova

```bash
mvn verify
```
