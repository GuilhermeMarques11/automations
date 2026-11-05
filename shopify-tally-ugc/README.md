# Automação de Conteúdo UGC (Shopify + Tally Forms)

## Contexto & Problema de Negócio
Uma loja virtual do segmento pet (Shopify) coleta histórias e fotos enviadas pelos próprios clientes com seus cachorros para alimentar o blog da marca com Conteúdo Gerado pelo Usuário (UGC). 

O processo anterior exigia que a equipe recebesse as respostas do formulário, copiasse os textos manualmente, formatasse o layout e criasse o post do zero no painel da Shopify.

## Arquitetura da Solução
Desenvolvimento de uma automação via **Make.com**, que escuta novos envios de formulário e cria automaticamente o rascunho do post no CMS da Shopify. Agora a equipe só tem o trabalho de publicar ou deletar as novas publicações no painel do Shopify.

## Fluxo de Execução:
- Trigger: O cliente final preenche e envia o formulário no site.
- Processamento & Tratamento: O Make intercepta a requisição via Webhoo e estrutura a formatação HTML do corpo do artigo com os dados enviados do fomulário.
- Ação: Chamada à REST API nativa da Shopify para criar um novo artigo no blog com o status definido como Rascunho (Draft).

## Impacto & Valor Gerado
- Redução de Esforço Manual a Zero: Eliminação total da necessidade de digitar, copiar ou formatar posts manualmente no painel administrativo.
- Fluxo de Aprovação Rápido (Human-in-the-Loop): A equipe da loja atua apenas como curadora final, precisando apenas revisar o rascunho e clicar em "Publicar" ou "Deletar".
- Ganho de Escala: Capacidade de processar dezenas de histórias de clientes em segundos sem demandar horas da equipe de marketing.

## Melhorias previstas
- Permitir a equipe aprovar ou não os novos posts por e-mail, sem precisar acessar o Shopify.

