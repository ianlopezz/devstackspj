# DevTasks

Aplicació web de gestió de tasques feta amb HTML, CSS i JavaScript. Permet crear, completar, eliminar i filtrar tasques, veure'n les estadístiques i conservar-les al navegador amb `localStorage`.

**Aplicació publicada:** https://ianlopezz.github.io/devstackspj/

## Instal·lació

```bash
cd devtasks
npm ci
```

Obre `devtasks/index.html` amb Live Server per executar l'aplicació localment.

## Tests

```bash
cd devtasks
npm test
```

Els tests de Vitest comproven `isValidTask`, `createTask`, `filterTasks` i `getTaskStats`.

## Arquitectura

- `devtasks/js/app.js` gestiona el DOM, els esdeveniments, la representació de les tasques i `localStorage`.
- `devtasks/js/taskManager.js` conté la lògica de negoci independent del navegador.
- `devtasks/tests/app.test.js` comprova les funcions de `taskManager.js` amb Vitest.

## GitHub Actions i Pull Requests

La branca `main` està protegida. Els canvis es treballen en branques `feature/*` i s'incorporen mitjançant una Pull Request. La CI s'executa en cada PR cap a `main`, instal·la les dependències i executa els tests.

El workflow `Deploy Web App to GitHub Pages` publica automàticament el contingut de `devtasks/` quan hi ha canvis a `main`.

## Dependències

Dependabot comprova setmanalment les dependències npm de `devtasks/` i les GitHub Actions definides als workflows.
