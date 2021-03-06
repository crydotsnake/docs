##### Eventos de pull request para repositórios bifurcados

{% note %}

**Observação:** fluxos de trabalho não são executados em repositórios privados quando você abre uma pull request de um repositório bifurcado.

{% endnote %}

Quando você cria uma pull request a partir de um repositório bifurcado para o repositório base, o {% data variables.product.prodname_dotcom %} envia o evento de `pull_request` para o repositório base e nenhum evento de pull request acontecerá no repositório bifurcado.

Fluxos de trabalho não são executados em repositórios bifurcados por padrão. Você deve habilitar o GitHub Actions na aba **Actions** (Ações) do repositório bifurcado.

{% if currentVersion == "free-pro-team@latest"%}
When a first-time contributor submits a pull request to a public repository, a maintainer with write access must approve running workflows on the pull request. For more information, see "[Approving workflow runs from public forks](/actions/managing-workflow-runs/approving-workflow-runs-from-public-forks)."
{% endif %}

{% data reusables.actions.forked-secrets %} As permissões para o `GITHUB_TOKEN` em repositórios bifurcados são somente leitura. Para obter mais informações, consulte "[Autenticação com o GITHUB_TOKEN](/actions/configuring-and-managing-workflows/authenticating-with-the-github_token)".

{% note %}

**Note:** Workflows triggered by {% data variables.product.prodname_dependabot %} pull requests are treated as though they are from a forked repository, and are also subject to these restrictions.

{% endnote %}
