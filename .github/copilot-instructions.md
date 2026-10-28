# Instruccions de Desenvolupament per a DevTasks

1. Arquitectura de mòduls i desacoblament:
- Tota la lògica de negoci (càlculs, validacions i filtratges) ha d'anar únicament a `devtasks/js/taskManager.js` utilitzant ES6 Modules (`export`).
- Les funcions de `taskManager.js` han de ser pures i no poden fer referència a `document`, `window` o `localStorage`.
- La manipulació del DOM, els esdeveniments d'interfície i la persistència corresponen exclusivament a `devtasks/js/app.js`.

2. Tests unitaris amb Vitest:
- Per a qualsevol funció nova o modificació a `taskManager.js`, afegeix proves unitàries a `devtasks/tests/app.test.js` fent servir Vitest (`describe`, `it`, `expect`).

3. Estil i qualitat del codi:
- Utilitza JavaScript modern (ES6+), noms descriptius i funcions clares.
- Evita variables globals innecessàries.
