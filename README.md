# claude-marketplace

Marketplace de plugins do Claude Code do Flavio Magacho: um só lugar para instalar e atualizar
tudo. Cada plugin continua no próprio repositório; aqui fica só o apontamento.

## Adicionar o marketplace

```
/plugin marketplace add magacho/claude-marketplace
```

Para receber as atualizações sozinho, ligue a atualização automática em `/plugin` →
Marketplaces → `magacho`.

## Plugins

| Plugin | O que faz | Instalar |
|---|---|---|
| `statusbar` | Statusline de duas linhas com diretório, branch, modelo, plano, contexto e franquias de uso. Depois de instalar, rode `/statusbar:setup`. | `/plugin install statusbar@magacho` |
| `vibe` | Refina demandas em specs, modulariza código e audita a base em um deck 360°. | `/plugin install vibe@magacho` |
| `harness` | Audita e instala harness (hooks, permissões, CLAUDE.md) em repositórios. | `/plugin install harness@magacho` |
| `magents` | Compara o custo real de um produto entre AliExpress, Mercado Livre, Shopee e Amazon. | `/plugin install magents@magacho` |

## Adicionar um plugin

Acrescente uma entrada em `.claude-plugin/marketplace.json` apontando para o repositório do
plugin pela URL HTTPS (`"source": "url"` quando o plugin está na raiz, `"git-subdir"` quando está
numa subpasta). Evite `"source": "github"`: com SSH configurado na máquina ele clona via SSH, e
quem não tem chave cadastrada no GitHub recebe `Permission denied (publickey)`. e valide com `claude plugin validate .` antes do commit.
