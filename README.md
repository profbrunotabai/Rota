# R.O.T.A. · site do mapa do Ensino Médio

Esta pasta é o site do mapa: o **Obsidian** edita as notas e o **Quartz** transforma as notas em site. O GitHub publica o site sozinho a cada envio, de graça.

## O que tem aqui
- `content/`: as notas do site (o cofre do Obsidian). É a única pasta que você mexe no dia a dia.
- `quartz.config.yaml`: título, cores e rodapé do site.
- `.github/workflows/deploy.yml`: a publicação automática.
- O resto é o Quartz. Não precisa mexer.

## Publicar pela primeira vez (uma vez só, uns 30 minutos)
1. **Crie uma conta no GitHub** em github.com. O nome de usuário entra no endereço do site: `https://seu-usuario.github.io/rota/`.
2. **Instale o GitHub Desktop** (desktop.github.com) e entre com essa conta.
3. **Descompacte o `rota.zip`** numa pasta fixa, por exemplo em Documentos. Vai surgir a pasta `rota`. Não a mova nem renomeie depois.
4. **Crie o repositório.** No GitHub Desktop: *File → Add local repository* e escolha a pasta `rota`. Ele vai avisar que a pasta ainda não é um repositório: clique em *create a repository* e depois em *Create repository*. Se aparecerem arquivos na aba *Changes*, escreva `Primeira versão` em *Summary* e clique em *Commit to main*.
5. **Publique o repositório.** Clique em *Publish repository*, **desmarque** *Keep this code private* (o GitHub Pages gratuito exige repositório público) e confirme.
6. **Ligue o GitHub Pages.** No github.com, abra o repositório e vá em *Settings → Pages*. Em *Build and deployment → Source*, escolha **GitHub Actions**.
7. **Rode a publicação.** Vá em *Actions → Publicar o site → Run workflow* e confirme. Em 3 a 5 minutos aparece um ✓ verde, e o site fica no ar em `https://seu-usuario.github.io/rota/`.

> A execução automática que acontece logo depois do passo 5 costuma terminar com ✗ vermelho, porque o Pages ainda não estava ligado. É normal: o passo 7 resolve.

## Abrir no Obsidian
1. Instale o Obsidian (obsidian.md). É grátis.
2. Clique em *Open folder as vault* e escolha a pasta **`rota/content`**, e não a pasta `rota` inteira.
3. Abra o *Graph view* para ver o mapa, colorido por nível.

## Publicar um nó (a rotina)
1. No projeto de IA, peça `/no FUN-06` ou `/da-aula FUN-06`.
2. No Obsidian, abra `funcoes/FUN-06.md`, apague tudo e cole o rascunho. Ele vem com `draft: true`, então ainda não aparece no site.
3. Edite com a sua voz, resolva todos os exercícios e teste em sala.
4. Quando estiver pronto: troque para `draft: false` e, nas `tags`, troque `em-construcao` por `pronto`.
5. No GitHub Desktop: escreva um resumo (ex.: `Publica FUN-06`), clique em *Commit to main* e depois em *Push origin*. O site atualiza em uns 5 minutos.

> **Enviar (Push) é publicar.** Só envie quando tudo o que está na pasta puder ir ao ar. Notas com `draft: true` não aparecem no site.

## Regras de escrita (para o site não quebrar)
- **Reais com barra:** escreva `R\$ 5,00`. Sem a barra, o site lê o cifrão como início de fórmula.
- **Fórmulas:** `$...$` no meio do texto e `$$...$$` em destaque. Decimal com vírgula: `$0{,}5$`.
- **Links:** `[[FUN-05|Função afim]]`. O nome do arquivo é o ID do nó.
- **Notas só para você:** `%% texto %%` aparece no Obsidian e some no site.
- **Gabarito escondido:** `> [!note]- Gabarito` vira um bloco que o aluno abre com um clique.
- **Imagens:** arraste para dentro da nota. O Obsidian guarda na pasta `anexos`.

## Antes de divulgar o link
- [ ] Preencher a página *Sobre* (`content/sobre.md`) com o seu nome.
- [ ] Confirmar a licença do conteúdo (sugerida: CC BY-NC-SA 4.0, citada no rodapé e na página *Sobre*).
- [ ] Ler o FUN-05, que já vem publicado como exemplo, e as 16 notas da Base do Fundamental.

## Mudar a aparência
- **Título, cores e rodapé:** em `quartz.config.yaml` (`pageTitle`, `theme → colors`, `footer → links`).
- **Página inicial:** `content/index.md`. **Página Sobre:** `content/sobre.md`.
- Dá para editar direto no github.com (abra o arquivo, clique no lápis e em *Commit changes*). Depois, no GitHub Desktop, clique em *Pull origin* antes de continuar trabalhando no computador.

## Se algo der errado
- **✗ vermelho em Actions:** abra a execução, clique no passo com erro e copie as últimas linhas. Cole numa conversa com a IA do projeto.
- **Erro sobre "environment protection rules":** em *Settings → Environments*, apague `github-pages` e rode a publicação de novo.
- **Página 404 logo depois de publicar:** espere 5 minutos e confira se *Settings → Pages → Source* está em *GitHub Actions*.
- **Fórmula aparecendo crua ou texto estranho:** procure um `R$` sem barra na nota.
- **O GitHub Desktop não deixa enviar:** clique em *Pull origin* e tente de novo.

## Perguntas comuns
- **Preciso instalar programação?** Não. A publicação roda no GitHub. Instalar o Node.js só serve para ver o site no próprio computador antes de enviar (opcional): `npm ci`, depois `npx quartz plugin install --from-config` e `npx quartz build --serve`, e abra `http://localhost:8080`.
- **E pelo celular?** Pequenas correções dá para fazer no github.com. Para escrever nós, use o computador.
- **Os rascunhos ficam visíveis?** Não no site, mas sim no repositório, que é público. Rascunhos que você não quer mostrar ficam fora da pasta `rota`.
- **Domínio próprio?** Em *Settings → Pages → Custom domain*. Depois troque `baseUrl` e o link "Sobre o projeto" em `quartz.config.yaml`.
- **Contagem de visitas?** Desligada (`analytics: null`). O público tem 15 a 17 anos; se for ligar, use um serviço sem cookies que só conte acessos agregados, e confirme antes com um advogado (ECA Digital e LGPD).

## Créditos e licenças
- Site gerado com o [Quartz 5](https://quartz.jzhao.xyz), licença MIT (`LICENSE.txt`).
- Conteúdo do mapa: licença a confirmar pelo autor (sugestão: CC BY-NC-SA 4.0).
