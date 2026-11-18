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
- **GitHub:** repo é público, então leitura (clone/pull) não precisa de login. **Push precisa de autenticação** — na primeira vez, o Git Credential Manager abre um fluxo de login no navegador padrão. O Marcos precisa fazer esse login uma vez (ele mesmo, nunca o Claude) para destravar pushes futuros sem precisar estar na máquina.
- **Netlify:** há um conector MCP (Netlify) já autorizado nesta sessão, com leitura confirmada (lista de projetos, deploys). Não é necessário login no Chrome para isso. Ações de escrita (redeploy manual, mudar configs) usam o mesmo conector, mas qualquer ação que afete produção é confirmada com o Marcos antes de executar.
- **Chrome (extensão real, claude-in-chrome):** conectado e funcional nesta sessão. Usado para conferir o site publicado visualmente, checar o dashboard do Netlify e, se preciso, telas do GitHub. Login do Marcos no GitHub/Netlify dentro desse Chrome ainda não estava feito em 2026-11-18 — pedido a ele para fazer esse login.

## Regra de publicação (não muda com a ausência do Marcos)

- Qualquer `git push` para `main` publica direto em produção (prayersforyoursoul.com), então **sempre é confirmado com o Marcos antes**, mesmo com ele fora do terminal — a confirmação chega por mensagem nesta sessão e ele responde remotamente quando puder.
- Mudanças ficam prontas (comitadas localmente) e descritas na sessão; o push só acontece depois do "sim" dele.

## Rotina de melhoria contínua (a definir com o Marcos / ajustar aqui conforme decidido)

- [ ] Frequência da revisão (reativa / semanal / junto da rotina diária de comentários)
- [ ] Escopo (só manter conteúdo sincronizado com episódios novos vs. também sugerir SEO/design/performance)
- [ ] Onde ficam os pedidos de oração e dedicatórias do site em relação à lista `Pedidos_de_Oracao_PFYS.md` já usada nos outros shows

## Histórico desta sessão

- 2026-11-18: localizado o projeto Netlify + repo GitHub (não havia cópia local no PC antes); clonado para `C:\Users\marco\Documents\prayersforyoursoul-site`; git configurado; este handoff criado como primeiro commit de teste do fluxo de push.
