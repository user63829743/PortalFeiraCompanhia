# Portal das Feiras — publicação no GitHub e Vercel

Este pacote está organizado em três projetos independentes, todos apontando para o mesmo repositório:

| Projeto Vercel | Root Directory |
|---|---|
| Portal público | `apps/portal-publico` |
| Cadastro de bancas | `apps/cadastro` |
| Painel administrativo | `apps/admin` |

Em cada projeto, mantenha o framework como **Other** e não altere o Output Directory. O arquivo `vercel.json` já encaminha as requisições para o handler serverless e os arquivos públicos continuam sendo servidos pelo servidor de cada aplicação.

Configure na Vercel as variáveis `SUPABASE_URL` e `SUPABASE_SECRET_KEY` nos três projetos. No Admin, configure também `ADMIN_USERNAME`, `ADMIN_PASSWORD_HASH` e `SESSION_SECRET` se esses nomes forem usados no seu arquivo de ambiente atual. Nunca envie `.env` ao GitHub.

Depois de importar o repositório, publique primeiro o Portal público, depois o Cadastro e por último o Admin. Após cada alteração visual, faça commit no GitHub e use **Redeploy** na implantação correspondente.

O link Anuncie da Home foi deixado relativo como `/cadastro/`, portanto, se Cadastro e Portal público forem projetos separados, substitua esse link pela URL final do projeto de Cadastro depois que ela for criada. O link TVegNews permanece externo.
