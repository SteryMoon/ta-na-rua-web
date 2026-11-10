# Tá na Rua – Painel web da prefeitura

Global Solution CitizenTech (FIAP) – parte **web** da solução Tá na Rua.

## Integrantes
- Stephanie da Silva Cruz – RM561341

## Descrição da solução
Painel usado pela prefeitura (ou ONG) para acompanhar as ocorrências enviadas pelos moradores pelo app. Nele é possível:
- ver todas as ocorrências em tempo real;
- filtrar por status (Todas, Abertas, Em andamento e Resolvidas);
- alterar o status de cada ocorrência.

**Plataforma publicada:** COLE_AQUI_O_LINK_DA_VERCEL

O aplicativo mobile está em outro repositório:
- Repositório do app: https://github.com/SteryMoon/ta-na-rua-app

## Como a integração funciona
App e web usam o mesmo banco **Firebase Firestore**, na coleção `ocorrencias`.
1. O cidadão cria a ocorrência no app (`status: "aberta"`).
2. Esta página recebe a nova ocorrência em tempo real (`onSnapshot`).
3. Ao mudar o status no painel, o documento é atualizado no Firestore e o app mostra a mudança na hora.

## Tecnologias
HTML, CSS e JavaScript puro, com Firebase Firestore. Publicado na Vercel.

## Motion design
- Entrada suave de cada ocorrência na lista.
- Destaque rápido no cartão que acabou de ser alterado.
- Botões com resposta ao clique.
- Animações desativadas para quem usa `prefers-reduced-motion`.

## Acessibilidade
- HTML semântico (`header`, `main`, listas) e idioma da página definido.
- Navegação completa pelo teclado, com foco visível.
- Status com texto e símbolo, nunca só cor.
- Avisos para leitor de tela quando o status muda (`aria-live`).
- Botões e campos com área de clique confortável e contraste alto.
- Layout responsivo para celular, tablet e computador.

## Como executar localmente
```bash
git clone https://github.com/SteryMoon/ta-na-rua-web.git
cd ta-na-rua-web
npx serve
```
Abra o endereço que aparecer (normalmente http://localhost:3000). Se a lista estiver vazia, clique em **Carregar ocorrências de exemplo**.

## ODS
**ODS 11 – Cidades e comunidades sustentáveis.** O painel dá transparência e agilidade à resposta do poder público aos problemas da cidade.
