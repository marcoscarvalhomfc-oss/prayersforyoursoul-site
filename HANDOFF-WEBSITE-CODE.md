# HANDOFF — Site PRAYERS (prayersforyoursoul.com) para o Claude Code

Este arquivo documenta a rotina de manutenção e melhoria contínua do site do PFYS, assumida por esta sessão do Claude Code (CODE) no PC do Marcos, para que ele possa acompanhar remotamente.

## Infraestrutura

- **Site ao vivo:** https://prayersforyoursoul.com
- **Hospedagem:** Netlify, projeto `prayersforyoursoul` (id `14228897-0160-4888-829e-507a9e8c24d7`), equipe `6a5d0ee2714d1448190df602`
- **Repositório:** https://github.com/marcoscarvalhomfc-oss/prayersforyoursoul-site (público, branch `main`)
- **Deploy:** push em `main` → Netlify faz rebuild/redeploy automático em produção. Até agora o histórico era só uploads manuais ("Add files via upload") pela interface web do GitHub.
- **Cópia local de trabalho:** `C:\Users\marco\Documents\prayersforyoursoul-site` (clonada em 2026-11-18). Site estático simples: `index.html` (tudo inline, sem build), `logo.png`, capas de episódio (`ep-*.jpg`, `episode-cover.jpg`). Sem package.json/build step.

## Acessos e permissões

- **Git:** instalado (2.55.0.windows.5), com Git Credential Manager (2.9.1) disponível como credential helper. Nenhuma config global existia antes; identidade local configurada no repo: `user.name = Marcos Carvalho`, `user.email = marcos.carvalho.mfc@gmail.com`.
- **GitHub:** repo é público, então leitura (clone/pull) não precisa de login. **Push precisa de autenticação** — o Git Credential Manager abre um fluxo de login na primeira vez. Feito e confirmado em 2026-11-18 (push de teste do próprio handoff foi aceito e o Netlify redeployou em seguida) — pushes futuros não precisam mais do Marcos presente na máquina.
- **Netlify:** há um conector MCP (Netlify) já autorizado nesta sessão, com leitura confirmada (lista de projetos, deploys) e deploy automático confirmado após o push de teste. Não é necessário login no Chrome para isso. Ações de escrita via conector (redeploy manual, mudar configs) que não sejam o fluxo normal de push ainda são confirmadas com o Marcos antes de executar.
- **Chrome (extensão real, claude-in-chrome):** conectado e funcional nesta sessão. Usado para conferir o site publicado visualmente, checar o dashboard do Netlify e, se preciso, telas do GitHub.

## Regra de publicação

- `git push` para `main` publica direto em produção (prayersforyoursoul.com).
- **Conteúdo simples** (textos, episódios, correções pontuais): pode publicar sem perguntar antes — decisão do Marcos em 2026-11-18.
- **Design/estrutura** (mudanças visuais, de layout ou de arquitetura do site): sempre pede confirmação antes do push, mesmo com o Marcos fora do terminal — a confirmação chega por mensagem nesta sessão e ele responde remotamente quando puder.

## Rotina de melhoria contínua

- **Frequência:** revisão periódica (decisão do Marcos em 2026-11-18, enquanto ele está fora).
- **Escopo:** conferir links, SEO básico e consistência do site com os episódios publicados; propor melhorias (design/estrutura sempre pede confirmação antes de publicar).
- **Monitoramento de tráfego:** via conector Netlify (`netlify-observability-services-reader`), que lê os access logs de borda direto do projeto — não precisa de Google Analytics nem de script de terceiros no site. Limitação: plano free do Netlify só guarda 24h de logs; para enxergar tendência ao longo do tempo é preciso registrar snapshots periodicamente (ainda não automatizado).
- [ ] Onde ficam os pedidos de oração e dedicatórias do site em relação à lista `Pedidos_de_Oracao_PFYS.md` já usada nos outros shows — ainda não decidido.

## Histórico desta sessão

- 2026-11-18: localizado o projeto Netlify + repo GitHub (não havia cópia local no PC antes); clonado para `C:\Users\marco\Documents\prayersforyoursoul-site`; git configurado; este handoff criado como primeiro commit de teste do fluxo de push.
- 2026-11-18: atualizada a seção "Recent episodes" (estava com episódios de julho) com os 6 mais recentes, dados reais via Spotify.
- 2026-11-19: adicionado SEO básico (Open Graph/Twitter cards, canonical, robots.txt, sitemap.xml, link de YouTube no footer — canal não estava linkado no site). Primeira leitura de tráfego via Netlify logs: tráfego real quase zero ainda (maioria é bot/scanner de WordPress e requisições sem referrer; nenhum referral vindo de YouTube/Spotify/redes sociais foi detectado). Donation/doações: investigado, aguardando decisão do Marcos sobre plataforma (ver seção abaixo quando criada).
- 2026-11-19 (rotina automática): 806 requests em 24h (698 browser; 569 são 404 de scanners/WordPress sem referrer). Nenhuma correção feita. Health-check ao vivo e links externos não verificados: prayersforyoursoul.com e hosts externos estão bloqueados na rede da sessão. Assets locais todos presentes no repo. Detalhes em traffic-log.md.
- 2026-11-20 (rotina automática): 851 requests em 24h (423 browser; 628 são 404 de scanners/WordPress sem referrer). Nenhuma correção feita, nenhuma sugestão nova. Health-check ao vivo e links externos não verificados (rede da sessão bloqueia os hosts); assets locais todos presentes. Detalhes em traffic-log.md.
