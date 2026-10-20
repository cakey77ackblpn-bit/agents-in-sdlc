---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar o pull request e confirmar que o Space Quiz está no ar."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que qualquer pessoa possa acessá-lo. O Copilot pode preparar o fluxo de trabalho e orientar a implantação, mas você é responsável por revisar as mudanças e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar uma implantação no GitHub Pages.
- revisar o fluxo de trabalho e o pull request antes de mesclá-lo.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas ainda falta uma forma simples de experimentá-lo. Publicar o site de um único arquivo com o GitHub Pages disponibiliza uma URL pública sem adicionar um servidor ou dependência de runtime.

## Peça ao Copilot para implantar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um fluxo de trabalho do GitHub Actions que compile o site, se necessário, e faça a implantação no GitHub Pages. Se ainda não houver um README, adicione um que descreva o aplicativo e como executá-lo localmente. Crie um pull request com essas mudanças e faça a mesclagem depois que as verificações obrigatórias forem aprovadas. Monitore a implantação até ela ser concluída com sucesso e, então, informe a URL final do site publicado. Se você não tiver permissão para habilitar o Pages ou mesclar, diga exatamente o que preciso aprovar ou fazer; não informe que deu certo até o site estar no ar.
```

![Diagrama de três etapas: pull request do space-quiz mesclado; execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e mescle um pull request e altere as configurações do Pages no repositório. Revise o diff, as permissões de implantação e quaisquer solicitações de aprovação do GitHub antes de continuar.

## Revise o fluxo de trabalho e confirme a implantação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as mudanças do pull request, incluindo as etapas de compilação e implantação do fluxo de trabalho.
3. Faça a mesclagem somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até ela ser concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou mesclar o pull request, siga as instruções específicas fornecidas. Não considere a tarefa concluída até a implantação ser bem-sucedida e o site carregar.

## Resumo e próximas etapas

O Space Quiz agora está disponível como um site publicado, e você verificou a implantação em vez de confiar apenas no relatório do agente. Continue para a [Lição 13: revisão e próximas etapas][next-lesson].

[next-lesson]: ../13-review/
