# Academia P5

Landing page frontend em React, Vite, TypeScript, Tailwind CSS, Framer Motion e Lucide React.

## Execução

Requer Node.js 22 ou superior e npm. Na pasta `/workspace/loja-criativo-teste-14`:

```sh
npm ci
npm run dev
```

O package-lock.json foi gerado; use `npm ci` para instalações reproduzíveis. `npm run build` verifica TypeScript e gera `dist`; `npm run preview` serve o build.

## Estrutura

```text
src/
  main.tsx
  App.tsx
  styles.css
  components/ui/
    prisma-hero.tsx
    container-scroll-animation.tsx
index.html
vite.config.ts
tsconfig.json
tailwind.config.js
postcss.config.js
```

## Dados a confirmar

Em `src/App.tsx`, preencher `academy.whatsapp` com número internacional somente com dígitos, `academy.address` e `academy.mapUrl` com URL oficial de incorporação do mapa. O WhatsApp só aparece quando configurado e monta a mensagem com encodeURIComponent; não confirma matrícula. O mapa só carrega após ação do visitante. Não há backend, formulários, login ou pagamento.

Modalidades, limites de alunos, valores, horários e endereço foram transcritos dos prints enviados pelo cliente. Os valores exibem aviso para confirmar vigência e disponibilidade. O WhatsApp não foi fornecido; o contato funcional aponta para @p5academia. A galeria é um marcador visual explícito, não uma fotografia da academia. Substituir por fotos reais autorizadas usando picture/img, WebP/AVIF, width/height, srcset/sizes e loading="lazy" abaixo da dobra. Nenhum vídeo, foto de banco ou contato foi inventado. Fonte: Arial/Helvetica local, sem download de fonte ou licença adicional.

## Validação

Executar `npm run build`. Iniciar `npm run dev` e conferir a resposta HTTP e o navegador. Testar 320, 375, 390, 430, 768, 1024, 1280, 1440 e 1920px: sem overflow horizontal, menu mobile, âncoras, skip link, foco visível e FAQ usando Tab/Enter/Espaço. O título deve entrar uma única vez com palavras escalonadas (0,08s); a galeria desktop deve girar de 20° a 0° e escalar de 1,05 a 1 ao rolar. No mobile a transformação é removida para legibilidade. Ativar redução de movimento e conferir título imediato e galeria estática. Após cadastrar contato real, conferir URL e mensagem do WhatsApp; após cadastrar mapa, confirmar que nenhuma requisição é enviada antes do clique.

## Estado da preparação

Dependências instaladas e build de produção aprovado. Chromium validou menu mobile, FAQ, redução de movimento, ausência de erros JavaScript e layouts nas nove larguras listadas (tolerância de 1px para arredondamento de transformações). Capturas desktop e mobile foram geradas e a desktop inspecionada. Vite iniciado na porta 5173. O sandbox impede conexões ao proxy e abertura de porta; essas operações funcionaram com execução escalada autorizada, preservando proxy e TLS. Não há suíte de testes preexistente.

O fundo usa dois clipes ilustrativos Mixkit com licença comercial gratuita verificada: salto na caixa e cordas de treino. Não são filmagens da Academia P5. Créditos, URLs e licença em `public/media/CREDITS.md`. Foram geradas versões locais H.264 sem áudio: desktop horizontal (6s, ~908 KB) e mobile vertical (12s, ~794 KB), com poster WebP, pausa e redução de movimento. A referência Evolua Club foi acessada após atualização de rede, sem copiar suas mídias. O antigo fundo abstrato continua disponível em disco, mas não é usado pela página.
