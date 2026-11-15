# Rota Ciclo Costeira / Coastal Cycle Route

[Aplicativo / Live app](https://saipradikmallakuntla-tech.github.io/rota-ciclo-costeira/)

PT: simulador educativo de tempo de pedal, com distância, velocidade, pausas e opção de volta. Interface, erros e resultados em PT/EN. Não traça rotas, não verifica ciclovias, clima, acessibilidade ou segurança. Nenhuma condição foi verificada em campo.

EN: educational cycling-time simulator with distance, speed, breaks and an optional return. PT/EN interface, errors and results. Not route navigation, a cycleway/weather/accessibility check, or a safety guarantee. No field verification.

## Run / Executar

Static HTML/CSS/JS with no build or external runtime dependencies. Serve this directory with `python3 -m http.server 8080`, then open http://localhost:8080/. GitHub Pages publishes `main` at `/`, with HTTPS enforced and no custom domain. `.nojekyll` disables Jekyll processing.

## Calculation / Cálculo

`total minutes = one-way km * (return ? 2 : 1) / km/h * 60 + total break minutes`.

Finite inputs only: distance 0.1–500 km; speed 1–60 km/h; total breaks 0–720 min. Breaks are not doubled on a return trip. Rounding is for display only. Pure logic is exported from `core.js` for Node tests. Example: 12 km / 15 km/h + 10 min = 58 min; return = 106 min.

Reference link selected 2026-11-15: https://www.gov.br/transportes/pt-br/assuntos/transito . Consult current local regulations; this is not legal advice. Selection date is not a field-validation or official data-update date.

No analytics, network API, geolocation, login or persistent form-data storage. Language uses `?lang=en`; no personal data is added to URLs. The page includes working HTML navigation when JavaScript is off. See [NETWORK.md](NETWORK.md) and the hub's release report for verification scope.
