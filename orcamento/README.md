# Orç¡¡amentos em Nós — Orca Fast

Editor visual de orç¡¡amentos estilo node-based para a loja de tintas e decoração.

## Como usar

### 1. Abrir o editor

Abra o arquivo [`orcamento-node-editor.html`](orcamento-node-editor.html) diretamente no navegador (Chrome, Edge, Firefox, etc.). Não precisa de servidor — basta abrir o arquivo localmente.

### 2. Adicionar caixas (ns)

Use os bot es na barra superior:

- **+ Cliente** — dados do cliente (nome, WhatsApp, vendedor)
- **+ Produto** — produto com volume, preç¡¡o original, preç¡¡o promocional, rendimento (mÂ²), quantidade
- **+ Promoç¡¡o** — nome da promoç¡¡o e percentual de desconto
- **+ Total** — orç¡¡amento consolidado (soma tudo que estiver conectado)

### 3. Conectar as caixas

1. Clique na **bolinha direita** (sa da) de um **Cliente** ou **Produto**
2. Clique na **bolinha esquerda** do **Total**
3. Para aplicar desconto: clique na sa da de **Promoç¡¡o** e depois na entrada **promo** de um **Produto**

Regras:
- **Cliente → Total** (personaliza a mensagem com nome do cliente)
- **Produto → Total** (adiciona itens ao orç¡¡amento)
- **Promoç¡¡o → Produto** (calcula preç¡¡o promocional autom tico)

### 4. Preencher dados

Em cada caixa:
- **Cliente:** nome, WhatsApp (DDI+DDD+n mero), vendedor (padr o: Afonso)
- **Produto:** nome, volume (ex: 18 L), preç¡¡o original, preç¡¡o promocional (ou deixe vazio para calcular autom tico), rendimento por unidade (mÂ²), quantidade
- **Promoç¡¡o:** nome, desconto (%)

### 5. Gerar orç¡¡amento

No n **Total**, voc ver:
- Lista de produtos conectados
- Total geral em R$
- Rendimento total estimado (mÂ²)
- Mensagem pronta para WhatsApp (modelo Afonso - consultor)

A es dispon veis:
- **Copiar** — copia a mensagem para a rea de transfer ncia
- **WhatsApp** — abre WhatsApp Web com a mensagem preenchida (usa o telefone do cliente se informado)
- **Imprimir** — abre janela de impress o para salvar como PDF ou imprimir

### 6. Salvar e carregar

- **Salvar** — guarda todo o layout e dados no armazenamento local do navegador
- **Carregar** — restaura o ltimo orç¡¡amento salvo
- **Limpar** — remove todas as caixas e conex es

## Exemplo de uso

1. Adicione um **Cliente** e preencha nome e WhatsApp
2. Adicione dois **Produtos** (ex: 18 L e 3,6 L) com preç¡¡os e rendimentos
3. (Opcional) Adicione uma **Promoç¡¡o** e conecte em um dos produtos
4. Adicione um **Total** e conecte: Cliente → Total, Produto → Total (ambos)
5. Veja o orç¡¡amento pronto e clique em **Copiar** ou **WhatsApp**

## Dicas

- Para editar um orç¡¡amento salvo, use **Carregar**, faça alteraç¡¡es e **Salvar** novamente
- Use nomes claros nos produtos (ex: "Tinta Acrí¡¡lica Premium 18 L") para facilitar a leitura da mensagem
- A mensagem gerada segue o padr o: saudaç¡¡o, apresentaç¡¡o como Afonso (consultor), lista de produtos com preç¡¡o e rendimento, total e encerramento
- O rendimento total é a soma dos rendimentos de todos os produtos (rendimento por unidade × quantidade)

## Estrutura de arquivos

```
orcamento/
├── README.md                      # Este arquivo
└── orcamento-node-editor.html    # Editor completo (HTML + CSS + JS em arquivo único)
```

## Personalizaç¡¡o (avanç¡¡o)

Se quiser adaptar:
- Edite o campo `vendedor` no n Cliente para mudar o nome do consultor
- Ajuste os valores padr o no código JavaScript (funç¡¡o `D`)
- Modifique o modelo da mensagem na funç¡¡o `calc()` para incluir mais detalhes (prazo, condiç¡¡es de pagamento, etc.)

---

**Autor:** Afonso Pereira  
**Local:** Santa Catarina, BR
