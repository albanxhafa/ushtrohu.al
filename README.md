# ushtrohu.al

Faqja hyrëse për **Ushtrohu 1 Minutë** — një aplikacion celular plotësisht jashtë linje për
pushime lëvizjeje njëminutëshe (shqip). Faqja në anglisht: [exercise1min.com](https://exercise1min.com).

Faqe statike — HTML, CSS dhe JS të thjeshta, pa hap ndërtimi, korniza apo asete të jashtme.
Publikohet në **GitHub Pages** me çdo push në `main` përmes `.github/workflows/deploy.yml`.

## Parapamje lokale

```bash
python3 -m http.server
# pastaj hap http://localhost:8000
```

## Publikimi

Çdo push në `main` nis `.github/workflows/deploy.yml`, i cili e publikon faqen në
**GitHub Pages** duke përdorur burimin e ndërtimit **GitHub Actions**.

Burimi i Pages i repo-s **duhet të jetë vendosur në "GitHub Actions"** (Settings → Pages →
Build and deployment → Source). Workflow-i i kalon `enablement: true` veprimit
`actions/configure-pages`, kështu që Pages aktivizohet automatikisht në një repo të re. Nëse
një ekzekutim dështon me `Get Pages site failed … Not Found`, do të thotë që Pages nuk ishte
aktivizuar kurrë — vendos burimin në GitHub Actions (ose ri-ekzekutoje kur `enablement: true`
të jetë në vend) dhe ri-nis workflow-in.

Domeni i personalizuar vendoset përmes skedarit `CNAME` (`ushtrohu.al`).
