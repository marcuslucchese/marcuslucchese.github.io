## Plan: Migrar conteúdo do site poliretribua.org.br para este repositório Hugo

TL;DR - Usar o repositório Hugo existente como base, adaptar a configuração e os layouts, e criar novos arquivos .md para refletir o conteúdo atual de poliretribua.org.br.

**Steps**
1. Auditar a estrutura atual do repositório Hugo. Verificar `hugo.toml`, `layouts/_default/single.html` e as páginas atuais em `content/`.
2. Mapear o conteúdo do site atual de poliretribua.org.br para páginas Hugo. Pelo menos precisarão de: Home, Quem Somos, Colabore/Doe, Privacidade/LGPD, Contato, possivelmente Depoimentos e Documentos para download.
3. Atualizar `hugo.toml` com novo `baseURL`, `title` e outras configurações relevantes para o site PoliRetribua.
4. Criar/atualizar arquivos Markdown em `content/` com frontmatter adequados e o texto extraído do site poliretribua.org.br.
5. Atualizar o layout em `layouts/_default/single.html` para refletir a navegação e estrutura do novo site, mantendo o design simples ou melhorando conforme necessário.
6. Verificar se existem páginas adicionais necessárias (por exemplo, `documentos-para-download`, `newsletter`, `depoimentos`) e criar conteúdo ou redirecionamentos apropriados.
7. Testar localmente com `hugo server` e validar URLs e navegação.

**Relevant files**
- `/home/marcus/codes/marcuslucchese.github.io/hugo.toml` — configurar o site Hugo e metadados.
- `/home/marcus/codes/marcuslucchese.github.io/layouts/_default/single.html` — adaptar o template de página para o novo site.
- `/home/marcus/codes/marcuslucchese.github.io/content/_index.md` — reescrever para a Home.
- `/home/marcus/codes/marcuslucchese.github.io/content/quem-somos.md` — conteúdo "Quem Somos".
- `/home/marcus/codes/marcuslucchese.github.io/content/contato.md` — conteúdo de contato.
- `/home/marcus/codes/marcuslucchese.github.io/content/projetos.md` — possível uso como página de Colabore ou Depoimentos.

**Verification**
1. Abrir o site localmente com `hugo server` e confirmar que as páginas Home, Quem Somos, Contato, Colabore e Privacidade aparecem.
2. Verificar navegação e links internos, especialmente se usar slugs como `/quem-somos/`, `/colabore/`, `/privacidade-e-protecao-de-dados/`.
3. Conferir o texto principal copiado do site atual e ajustar para corresponder ao tom e seções reais do PoliRetribua.

**Decisions**
- O repo atual é um Hugo básico com quatro páginas; a migração pode ser feita usando a mesma estrutura de templates e criando novas páginas de conteúdo.
- A página inicial atual será substituída pelo conteúdo de `poliretribua.org.br`, com foco em campanhas, missão, valores e links de doação.
- Pode ser necessário criar novas páginas ou seções que não existiam no repositório original, como `colabore`, `privacidade-e-protecao-de-dados` e possivelmente `documentos-para-download`.

**Further Considerations**
1. Preciso saber se você quer usar o mesmo visual simples do template atual ou criar um design mais fiel ao site existente.
2. Confirme se devemos preservar URLs iguais aos do site atual (por exemplo, `/colabore/` e `/privacidade-e-protecao-de-dados/`).
3. Se houver mais conteúdo importante em poliretribua.org.br, indique as páginas ou forneça os textos para completar a migração.