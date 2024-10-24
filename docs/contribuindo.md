# Contribuindo para a Documentação do MT Awesome Data

Obrigado por considerar contribuir para a **Documentação do MT Awesome Data**! Nossa documentação é mantida de forma colaborativa para garantir que forneça informações precisas, atualizadas e úteis para todos os membros do time de dados da Meutudo (MT).

Este guia tem como objetivo facilitar sua contribuição, explicando como você pode adicionar ou atualizar páginas na documentação automatizada utilizando o **MkDocs** e o fluxo de trabalho estabelecido com as branches `main` e `homolog`.

## Índice

- [Pré-requisitos](#pré-requisitos)
- [Passo a Passo para Contribuir](#passo-a-passo-para-contribuir)
  - [1. Fork e Clone do Repositório](#1-fork-e-clone-do-repositório)
  - [2. Configurar o Ambiente de Desenvolvimento](#2-configurar-o-ambiente-de-desenvolvimento)
  - [3. Criar uma Branch para Sua Contribuição](#3-criar-uma-branch-para-sua-contribuição)
  - [4. Adicionar ou Atualizar a Documentação](#4-adicionar-ou-atualizar-a-documentação)
  - [5. Testar as Alterações Localmente](#5-testar-as-alterações-localmente)
  - [6. Commitar e Push das Alterações](#6-commitar-e-push-das-alterações)
  - [7. Abrir um Pull Request](#7-abrir-um-pull-request)
- [Processo de Code Review](#processo-de-code-review)
  - [Uso de CODEOWNERS](#uso-de-codeowners)
  - [Requisitos para o Merge](#requisitos-para-o-merge)
- [Boas Práticas de Contribuição](#boas-práticas-de-contribuição)
- [Recursos Adicionais](#recursos-adicionais)
- [Código de Conduta](#código-de-conduta)

## Pré-requisitos

Antes de começar, certifique-se de ter o seguinte instalado em sua máquina:

- **Git**: Para controle de versão e integração com o GitHub.
- **Python** (versão 3.6 ou superior): Necessário para executar o MkDocs.
- **MkDocs**: Ferramenta para gerar a documentação.
- **MkDocs Material** (opcional): Tema para uma aparência moderna da documentação.

### Instalando o MkDocs e o Tema Material

1. **Instalar o MkDocs:**

   ```bash
   pip install mkdocs
   ```

2. **Instalar o Tema Material (opcional, mas recomendado):**

   ```bash
   pip install mkdocs-material
   ```

## Passo a Passo para Contribuir

### 1. Fork e Clone do Repositório

1. **Faça um Fork do Repositório:**

   - Navegue até o repositório [meutudo/mt-awesome-data](https://github.com/meutudo/mt-awesome-data) no GitHub.
   - Clique no botão **"Fork"** no canto superior direito para criar uma cópia do repositório na sua conta.

2. **Clone o Repositório Forked:**

   Abra o terminal e execute:

   ```bash
   git clone https://github.com/seu-usuario/mt-awesome-data.git
   cd mt-awesome-data
   ```

   > **Nota:** Substitua `seu-usuario` pelo seu nome de usuário no GitHub.

### 2. Configurar o Ambiente de Desenvolvimento

1. **Criar um Ambiente Virtual (Recomendado):**

   ```bash
   python -m venv venv
   ```

2. **Ativar o Ambiente Virtual:**

   - **No Windows:**

     ```bash
     venv\Scripts\activate
     ```

   - **No macOS/Linux:**

     ```bash
     source venv/bin/activate
     ```

3. **Instalar as Dependências:**

   ```bash
   pip install --upgrade pip
   pip install mkdocs mkdocs-material
   ```

### 3. Criar uma Branch para Sua Contribuição

Sempre crie uma nova branch para cada contribuição para manter o histórico de commits organizado.

```bash
git checkout -b feature/adicionar-faq
```

> **Boas Práticas de Nomeação:**
>
> - Use nomes descritivos e concisos.
> - Inclua o tipo de alteração e uma breve descrição.
>
> **Exemplos:**
>
> - `feature/adicionar-faq`
> - `docs/atualizar-tutorial-login`

### 4. Adicionar ou Atualizar a Documentação

1. **Navegue até a Pasta de Documentação:**

   ```bash
   cd docs/recursos/
   ```

2. **Criar ou Editar o Arquivo `faq.md`:**

   - **Para adicionar uma nova página:**

     ```bash
     touch faq.md
     ```

   - **Adicionar Conteúdo ao `faq.md`:**

     Abra o arquivo `faq.md` no seu editor de texto favorito e adicione o conteúdo desejado.

     **Exemplo de Conteúdo:**

     ```markdown
     # FAQ - Perguntas Frequentes

     ## 1. Como posso contribuir para a documentação?

     Para contribuir, siga o [guia de contribuição](../contribuindo.md). Crie uma branch, adicione ou atualize a documentação e abra um Pull Request.

     ## 2. Quem são os responsáveis pelas revisões de código?

     As revisões são feitas pelos membros designados no arquivo [CODEOWNERS](../CODEOWNERS).

     ## 3. Quais são as melhores práticas para escrever documentação?

     - Seja claro e conciso.
     - Utilize formatação adequada.
     - Mantenha os exemplos atualizados.
     - Revise ortografia e gramática.

     ## 4. Como reportar um erro na documentação?

     Abra uma [Issue](https://github.com/meutudo/mt-awesome-data/issues) descrevendo o erro encontrado com detalhes suficientes para reprodução.
     ```

### 5. Testar as Alterações Localmente

Antes de enviar suas alterações, é importante verificar se tudo está funcionando corretamente.

1. **Iniciar o Servidor de Desenvolvimento do MkDocs:**

   ```bash
   mkdocs serve
   ```

2. **Visualizar a Documentação:**

   Abra o navegador e acesse [http://127.0.0.1:8000/](http://127.0.0.1:8000/) para ver as alterações em tempo real.

   > **Dica:** O servidor de desenvolvimento recarrega automaticamente a página sempre que você salva alterações nos arquivos Markdown ou no `mkdocs.yml`.

### 6. Commitar e Push das Alterações

1. **Adicionar os Arquivos Modificados:**

   ```bash
   git add docs/recursos/faq.md
   ```

2. **Fazer o Commit das Alterações:**

   ```bash
   git commit -m "Adiciona página FAQ à seção Recursos"
   ```

3. **Push para o Repositório Forked:**

   ```bash
   git push origin feature/adicionar-faq
   ```

### 7. Abrir um Pull Request

1. **Acesse o Repositório Forked no GitHub:**

   Navegue até o seu repositório forked, por exemplo, [seu-usuario/mt-awesome-data](https://github.com/seu-usuario/mt-awesome-data).

2. **Iniciar um Novo Pull Request:**

   - Clique no botão **"Compare & pull request"**.
   - **Base Branch:** Selecione a branch `homolog`.
   - **Compare Branch:** Deve ser a branch que você criou, por exemplo, `feature/adicionar-faq`.

3. **Preencher o Título e a Descrição do PR:**

   - **Título:** Seja claro e descritivo.
   - **Descrição:** Explique o que foi alterado, por que foi necessário e quaisquer detalhes relevantes.

   **Exemplo de Título:**

   ```
   Adiciona página FAQ à seção Recursos
   ```

   **Exemplo de Descrição:**

   ```
   ### Descrição
   Esta PR adiciona uma nova página `faq.md` à seção **Recursos** da documentação. A página inclui respostas para perguntas frequentes do time de dados.

   ### Mudanças Realizadas
   - Criação do arquivo `docs/recursos/faq.md` com conteúdo inicial.
   - Atualização do arquivo `mkdocs.yml` para incluir a nova página na navegação.

   ### Referências
   - Issue #15 (se aplicável)
   ```

4. **Enviar o Pull Request:**
   - Clique em **"Create pull request"** para enviar sua contribuição.

## Processo de Code Review

### Uso de CODEOWNERS

O arquivo `CODEOWNERS` define quais membros ou equipes são responsáveis por revisar mudanças em determinadas partes do repositório. Quando um Pull Request (PR) altera arquivos cobertos pelo `CODEOWNERS`, os revisores designados são automaticamente adicionados como revisores do PR.

**Exemplo de `CODEOWNERS`:**

```plaintext
# Dono para toda a base de código
* @dev-team

# Dono para arquivos de documentação
/docs/* @documentacao
```

### Requisitos para o Merge

Para que um Pull Request seja mesclado na branch `homolog`, os seguintes requisitos devem ser atendidos:

1. **Aprovações Mínimas:**

   - **Pelo menos 2 aprovações** de revisores designados no `CODEOWNERS`.

2. **Resolução de Conflitos:**

   - Todos os **conflitos** entre a branch de origem (`feature`) e a branch de destino (`homolog`) devem ser **resolvidos** antes do merge.

3. **Sem Verificações Pendentes:**
   - Certifique-se de que todas as **verificações automáticas** (como testes e linting) passaram com sucesso.

### Fluxo de Code Review

1. **Revisores Recebem a Notificação:**

   - Os revisores designados são automaticamente solicitados a revisar o PR.

2. **Revisores Analisam as Alterações:**

   - Verificam a qualidade e a aderência aos padrões do projeto.
   - Validam a precisão e a clareza da documentação.

3. **Fornecem Feedback:**

   - **Aprovações:** Se tudo estiver conforme esperado.
   - **Solicitação de Mudanças:** Se houver melhorias a serem feitas.

4. **Autor do PR Realiza as Alterações:**

   - Faz as modificações solicitadas.
   - Atualiza o PR com os novos commits.

5. **Revisores Reavaliam as Alterações:**

   - Garantem que as solicitações de mudanças foram atendidas.

6. **Merge do Pull Request:**
   - Após obter as aprovações necessárias e resolver os conflitos, o PR pode ser mesclado na branch `homolog`.

## Boas Práticas de Contribuição

### 1. Escreva um Título e Descrição Claros

- **Título:** Deve resumir a alteração de forma concisa.
- **Descrição:** Deve fornecer contexto e detalhes suficientes sobre o que foi alterado e por quê.

### 2. Mantenha a Documentação Organizada

- Siga a estrutura existente do projeto.
- Use cabeçalhos, listas e formatação adequada para melhorar a legibilidade.

### 3. Use Links Relativos

- Utilize links relativos para referenciar outras páginas da documentação.

  **Exemplo:**

  ```markdown
  Para mais informações, consulte a [Página de Contribuição](contribuindo.md).
  ```

### 4. Verifique Ortografia e Gramática

- Revise o texto para evitar erros que possam comprometer a clareza da documentação.

### 5. Teste Localmente

- Antes de enviar o PR, utilize o `mkdocs serve` para verificar como as alterações aparecem no site.

### 6. Seja Respeitoso e Construtivo no Feedback

- Ao revisar PRs, forneça feedback de forma respeitosa e construtiva, focando em melhorar a documentação.

## Recursos Adicionais

- **[Documentação Oficial do MkDocs](https://www.mkdocs.org/):** Para aprofundar-se nas funcionalidades e configurações do MkDocs.
- **[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/):** Documentação e exemplos para o tema Material.
- **[GitHub Pages](https://docs.github.com/en/pages):** Guia oficial para configurar e gerenciar GitHub Pages.
- **[GitHub CODEOWNERS](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners):** Informações sobre como configurar o arquivo CODEOWNERS.

---

**Obrigado por contribuir para a Documentação do MT Awesome Data! Sua participação é fundamental para manter nossa documentação atualizada e útil para todos os membros do time de dados. Se tiver dúvidas ou precisar de assistência durante o processo de contribuição, não hesite em abrir uma Issue ou entrar em contato com a equipe.**
