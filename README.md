# Finanças Pessoais

App de controle financeiro pessoal: contas, cartões e faturas, despesas fixas e recorrentes, valores divididos com terceiros, vale-refeição, gastos da moto, metas, calendário, relatórios e projeções.

É um **PWA**: instala na tela inicial do celular (Android e iPhone), abre em tela cheia como um aplicativo e funciona sem internet.

## Onde ficam os dados

- Os dados ficam **somente no celular** em que o app foi instalado.
- **Nada é enviado ao GitHub.** O repositório guarda só o código.
- **Nunca envie o backup (.json) para o repositório.** O `.gitignore` já bloqueia arquivos `.json`.

## Arquivos (todos na raiz, sem subpastas)

| Arquivo | Para que serve |
|---|---|
| `index.html` | O app completo |
| `manifest.webmanifest` | Nome, cores e ícones para instalar |
| `sw.js` | Permite abrir sem internet |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Ícones do app |
| `.nojekyll` | Faz o GitHub Pages publicar os arquivos como estão |
| `.gitignore` | Impede o envio de backups ao GitHub |

Não há subpastas, então o upload funciona também pelo celular. Se algum arquivo faltar, o `index.html` usa uma configuração de instalação embutida.

## 1. Atualizar ou publicar no GitHub Pages

1. No repositório, **apague a pasta `icons`** e os arquivos antigos, se existirem.
2. Clique em **Add file → Upload files** e envie todos os arquivos desta pasta. Clique em **Commit changes**.
3. Em **Settings → Pages**, deixe **Branch: main** e pasta **/ (root)**.
4. Aguarde 1 a 2 minutos. O endereço fica assim: `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`

## 2. Instalar no celular

**Android (Chrome)**
1. Abra o endereço no Chrome. Se já tinha aberto antes, recarregue a página.
2. Toque no botão **⇩ Instalar app**, no topo do app, e confirme. Ou use **⋮ → Instalar app**.
3. O ícone aparece na tela inicial. Abra por ele: o app fica em tela cheia.

**iPhone (Safari)**
1. Abra o endereço no **Safari**.
2. Toque em **Compartilhar → Adicionar à Tela de Início**.

## 3. Carregar seus dados

1. Abra o app instalado. Na primeira vez, aparece a tela de boas-vindas.
2. Toque em **Importar backup** e escolha o arquivo `financas-pessoais-backup-AAAA-MM-DD.json`.
3. Confirme. Os lançamentos, contas, cartões, recorrências, metas e dados da moto aparecem.

## 4. Backup

- Exporte com frequência em **Categorias e dados → Backup (JSON)**. O app avisa quando o último backup tem mais de 7 dias.
- Desinstalar o app ou limpar os dados do Chrome **apaga os dados** do celular. Guarde os backups no Drive ou no e-mail.
- Para levar os dados entre o artefato e o celular, exporte o backup de um lado e importe do outro.

## 5. Atualizar o app

1. Substitua os arquivos no repositório.
2. No `sw.js`, aumente a versão em `const CACHE='fp-v1.2.0'` (por exemplo, para `fp-v1.2.1`).
3. No celular, feche e abra o app duas vezes. Os dados não são afetados.
