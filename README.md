window.webpackChunkdiscord_app.push([
  [Math.random()],
  {},
  req => {
    if (!req.c) return;
    for (const m of Object.keys(req.c)
      .map(x => req.c[x].exports)
      .filter(x => x)) {
      if (m.default && m.default.getToken !== undefined) {
        return copy(m.default.getToken());
      }
      if (m.getToken !== undefined) {
        return copy(m.getToken());
      }
    }
  },
]);
const consoleStyles = [
  'font-size: 16px',
  'background-color: #2a2a2a',
  'color: #1ed760',
  'padding: 8px',
  'border-radius: 4px',
  'font-weight: bold',
].join(';');

console.log('%c token copiado com sucesso', consoleStyles);
