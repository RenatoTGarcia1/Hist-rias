# Como publicar este site no GitHub Pages

Este repositório contém um site estático na pasta `site_EDS/`.

O repositório já inclui um workflow do GitHub Actions (`.github/workflows/pages.yml`) que publica o conteúdo de `site_EDS/` no branch `gh-pages` usando o token padrão `${{ secrets.GITHUB_TOKEN }}`.

Passos para publicar:

1. Adicione e comite os arquivos que foram criados ou alterados:

   git add .github/.nojekyll README_DEPLOY.md
   git commit -m "Add GitHub Pages workflow and deploy helpers"

2. Dê push para o branch `main`:

   git push origin main

3. O workflow será executado automaticamente e criará/atualizará o branch `gh-pages` com o conteúdo de `site_EDS/`.

4. Acesse seu site em: `https://<usuario>.github.io/<repo>/`

   - Substitua `<usuario>` pelo nome do dono do repositório (ex: RenatoTGarcia1)
   - Substitua `<repo>` pelo nome do repositório (ex: Hist-rias)

Observações:

- Se preferir usar um domínio customizado, crie um arquivo `CNAME` com seu domínio dentro de `site_EDS/` antes do deploy.
- Se quiser publicar diretamente da pasta `docs/` ou do branch `main` sem o workflow, pode configurar isso nas configurações do repositório em GitHub → Settings → Pages.
