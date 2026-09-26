# COVAFOG — Bancada de Cálculo

Ferramenta didática para foguetes de garrafa PET com propulsão por vinagre e bicarbonato,
usada na **Copa Vale do Aço de Foguetes (COVAFOG)**.

## O que ela faz

Dado o volume e a acidez do vinagre, a massa de bicarbonato, a garrafa e as medidas da base,
a bancada calcula **até onde a pressão daquela carga pode chegar** — o limite químico da reação.

O aluno informa o que o manômetro está marcando e a barra mostra quanto da reação já foi
liberada. Enquanto faltar pressão, vale agitar a garrafa. Quando o ganho por ciclo de agitação
cair abaixo de 5 psi, a reação acabou.

## Por que o manômetro marca menos

Quando a camisinha estoura, o bicarbonato tende a empedrar e a reação trava no meio. Parte do
CO₂ também fica dissolvido no líquido. Agitar quebra a crosta e libera o resto. A diferença
entre o número da bancada e o do manômetro é exatamente isso — não é erro de cálculo.

## Como usar

**No celular Android (instalar como app):**
abra https://dogdosliinks-tech.github.io/covafog-bancada/ no Chrome e toque em
**Instalar app** (no topo da bancada) ou no menu ⋮ → **Instalar app / Adicionar à tela inicial**.
O ícone da Bancada aparece junto dos outros apps e funciona **sem internet** depois de instalado.

**No computador:** abra o `index.html` no navegador. Não precisa instalar nada, nem estar conectado.

## Privacidade e segurança

- Arquivo único, sem dependência externa: nenhum script, fonte ou imagem de terceiros.
- Não usa `fetch`, `XMLHttpRequest`, cookies, `localStorage` ou `sessionStorage` no código da bancada.
- O `sw.js` (service worker) só guarda em cache os arquivos do próprio app, para funcionar offline
  depois de instalado. Não guarda nem envia nenhum dado de quem usa.
- Não coleta, não armazena e não transmite dado nenhum. Tudo roda no navegador de quem abre.
- A ficha de campo existe só enquanto a aba estiver aberta; copie ou imprima antes de fechar.
- `Content-Security-Policy` declarada no próprio HTML bloqueia carregamento externo
  (só libera arquivos do próprio site: manifesto, ícones e service worker).

Se for modificar, mantenha essas características — é o que torna seguro publicar a página
como site estático.

## Segurança no lançamento

Os valores são estimativas para uso **didático e supervisionado**, não leituras de instrumento.
A pressão real manda sempre. Garrafa PET de refrigerante trabalha com folga até cerca de
100–120 psi; acima disso o risco cresce rápido e a garrafa precisa ser nova e sem arranhões.
A bancada avisa quando a carga montada pode ultrapassar o limite informado.

## Licença

MIT — veja `LICENSE`.
