# Orca Fast

Gerador de orç¡¡amentos visuais em estilo node-based para loja de tintas e decoração.

## Vis o geral

O Orca Fast permite criar orç¡¡amentos profissionais arrastando e conectando caixas (ns) de Cliente, Produto, Promoç¡¡o e Total. O sistema calcula automaticamente valores, descontos, rendimentos e gera mensagens prontas para WhatsApp.

## Uso r pido

1. Abra o arquivo [`orcamento/orcamento-node-editor.html`](orcamento/orcamento-node-editor.html) diretamente no navegador
2. Adicione caixas usando os bot es no topo: **Cliente**, **Produto**, **Promoç¡¡o**, **Total**
3. Conecte as caixas: clique na bolinha direita (sa da) e depois na bolinha esquerda (entrada) do destino
4. Preencha os dados nos campos de cada caixa
5. O Total calcula automaticamente e gera a mensagem para envio

## Regras de conex o

- **Cliente** → **Total** (obrigat rio para personalizar a mensagem)
- **Produto** → **Total** (adiciona itens ao orç¡¡amento)
- **Promoç¡¡o** → **Produto** (aplica desconto autom tico no preç¡¡o)

## Funcionalidades

- Editor visual estilo node-based (sem depend ncias)
- C lculo autom tico de subtotal, total e rendimento em mÂ²
- Aplicaç¡¡o de descontos autom tica via conex o Promoç¡¡o → Produto
- Geraç¡¡o de mensagem personalizada para WhatsApp (modelo Afonso - consultor)
- Bot es: Copiar, WhatsApp, Imprimir
- Salvar/Carregar localmente no navegador

## Estrutura do reposit rio

```
orca-fast/
├── README.md                 # Este arquivo
├── orcamento/
│   ├── README.md            # Instruç¡¡es detalhadas do editor
│   └── orcamento-node-editor.html  # Editor completo
```

## Pr ximos passos (opcional)

- Ativar GitHub Pages para acessar via URL p blica
- Adicionar cat logo de produtos em JSON
- Integraç¡¡o com APIs de CRM ou WhatsApp Business
- Exportaç¡¡o de orç¡¡amentos em PDF

## Licenç¡¡

Uso livre para projetos pessoais e comerciais.

---

**Autor:** Afonso Pereira  
**Contato:** [adicionar contato]  
**Local:** Santa Catarina, BR
