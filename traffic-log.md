# PFYS — Traffic log (Netlify, janela de 24h)

## 2026-11-22
- Total: 841 requests nas últimas 24h (vs 3.202 ontem — pico de scanners passou).
- Por categoria: browser 665, tooling 80, other 58, crawler 34, ai-agent 3, page-preview 1.
- Status: 404 = 343, 200 = 203, 301 = 203, 304 = 92. Sem 5xx.
- Top URLs: https:// / (59), /logo.png (31), ep-invisible/overthinking/clear-mind/courage/scattered/rejection.webp (16 cada), /hero-hands.webp (15), http:// / (11).
- Top referrers: vazio (616, 342 deles com erro/404 = scanners), o próprio site (130), ~10 deploy previews *.netlify.app (8 cada). Nenhum referral de Spotify/YouTube/Apple.
- Health-check ao vivo e links externos NÃO executados: curl falhou (000) para todos os hosts — rede da sessão bloqueia. Local: todos os assets relativos do index.html (e hero-hands.webp) existem no repo. Nada quebrado detectado.

## 2026-11-21
- Total: 3.202 requests nas últimas 24h (vs 851 ontem) — salto de ~3,8x, quase todo scanner.
- Por categoria: sem categoria 2.463, other 642, browser 77, tooling 16, crawler 4.
- Status: 301 = 1.591, 429 = 1.229 (novo; rate-limit sobre scanners buscando backup.zip, dump.rar, database.sql etc.), 404 = 337, 200 = 45. Block reasons: nenhum.
- Top URLs: https:// / (25), http:// / (13), /wp-admin/install.php (12 em https + 12 em http), www / (9), /xmlrpc.php (4), /backup.zip (4).
- Top referrers: vazio (3.138), www.google.com (24), o próprio site (14), http://prayersforyoursoul.com (8), deploy preview *.netlify.app (7). Nenhum referral de Spotify/YouTube/Apple.
- Health-check ao vivo e links externos NÃO executados: curl falhou (000) para o site e todos os hosts externos — rede da sessão bloqueia. Local: todos os assets relativos do index.html existem no repo. Nada quebrado detectado.

## 2026-11-20
- Total: 851 requests nas últimas 24h (vs 806 ontem).
- Por categoria: browser 423, other 343, crawler 51, tooling 29, page-preview 4, ai-agent 1.
- Status: 404 = 628 (74%), 200 = 149, 301 = 62, 304 = 12 — de novo scanner sem referrer (ex.: /wp-admin/install.php ×12 em https + ×12 em http).
- Top URLs: / (64), http:// / (20), /logo.png (13), www / (12), /robots.txt (11), ep-rejection/invisible/overthinking.webp (10 cada).
- Top referrers: vazio (730), o próprio site (71), http://prayersforyoursoul.com (9), www (7), deploy previews *.netlify.app (7 cada), facebook.com (2). Nenhum referral de Spotify/YouTube/Apple.
- Health-check ao vivo e links externos NÃO executados: prayersforyoursoul.com e hosts externos bloqueados pela rede da sessão. Local: todos os assets relativos do index.html existem no repo. Nada quebrado detectado.

## 2026-11-19
- Total: 806 requests nas últimas 24h.
- Por categoria: browser 698, tooling 63, other 32, crawler 13.
- Status: 404 = 569 (71%), 200 = 192, 301 = 38, 304 = 7 — pico de 404 sem referrer, padrão de scanner (ex.: /wp-admin/install.php ×11 em https).
- Top URLs: / (60), /logo.png (25), http:// / (12), /wp-admin/install.php (11+11), ep-scattered/clear-mind/courage.webp (7 cada).
- Top referrers: vazio (654), o próprio site (86), http://prayersforyoursoul.com (8), www (7), URLs de deploy preview *.netlify.app (vários, 7 cada). Nenhum referral de Spotify/YouTube/Apple.
- Health-check ao vivo NÃO executado: domínio bloqueado pela política de rede da sessão (403 do proxy). Verificação local: todos os assets relativos do index.html existem no repo.
