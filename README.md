# ushtrohu.al

Faqe me ushtrime të thjeshta një-minutëshe në shqip - një rutinë për fillestarë, 48
ushtrime pa pajisje dhe një ftesë për të shkarkuar aplikacionin celular. E optimizuar për
SEO shqip (fjalët kyçe: *ushtrime në shtëpi, ushtrime pa pajisje, ushtrime për barkun,
ushtrime për këmbë, ushtrime për vithe, ushtrime për krahë, kardio në shtëpi*).

Ky sajt (**ushtrohu.al**) është faqe e pavarur për ushtrime një-minutëshe në shqip. E
vetmja ftesë jashtë përmbajtjes është drejt **aplikacionit celular** (së shpejti për
iOS & Android).

Faqe statike — HTML, CSS dhe JS të thjeshta, pa hap ndërtimi, korniza apo asete të jashtme.
Përmban të dhëna të strukturuara JSON-LD (`WebSite`, `WebPage`, `HowTo`, `ItemList`, `FAQPage`) për
kuptim më të qartë nga crawler-at dhe motorët e kërkimit. Publikohet në **GitHub Pages** me çdo push në `main` përmes
`.github/workflows/deploy.yml`.

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
