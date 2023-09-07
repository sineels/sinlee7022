---
제목: GitHub Codespaces 개요
짧은 제목: 개요
도입부: '이 가이드는 {% 데이터 변수를 소개합니다.product.prodname_github_codespace %}를 소개하고 그것이 어떻게 작동하는지 및 어떻게 사용하는지에 대한 세부 사항을 제공합니다.'
'제목 투 디퍼 프롬 파일 이름' 허용: 사실
redirect_from:
  - /codespace/codespaces-reference/about-codespace
  - /github/developing-online-with-github-codespace/about-github-codespace
  - /github/개발-온라인-with-codespace/about-codespace
  - /codespace/getting-started-with-codespace/about-codespace
  - /codespace/about-codespace
버전:
 fpt: ' *'
 게크: ' *'
유형: 개요
주제:
  - 코드스페이스
---

## 코드스페이스는 무엇입니까?

코드스페이스는 클라우드에서 호스트되는 개발 환경입니다. {% data 변수.product.prodname_github_codespace %}에 대한 프로젝트를 커스터마이징할 수 있습니다. [구성 파일](/codespaces/seting-up-your-project-for-codespace/ading-a-dev-container-Configuration/Introduction-to-dev-containers) 당신의 모든 사용자에게 반복 가능한 코드 공간 구성을 생성하는 저장소 (흔히 코드로 구성)로.

당신이 생성하는 각 코드스페이스는 가상 머신에서 실행되는 도커 컨테이너에서 {% 데이터 변수.product.prodname_dotcom %}에 의해 호스트됩니다. 가상 머신 타입 선택 중 2개의 코어, 8GB 램, 32GB 스토리지 중 최대 32개의 코어, 64GB 램, 128GB 스토리지 중에서 선택할 수 있다.

기본적으로 코드스페이스는 인기 언어와 도구의 선택을 포함하는 우분투 리눅스 이미지에서 생성되지만, 선택한 리눅스 배포를 기반으로 이미지를 사용하고 특정 요구 사항에 맞게 구성할 수 있다. 로컬 운영 체제와 상관없이 코드스페이스는 리눅스 환경에서 실행됩니다. 윈도우와 맥OS는 원격 컨테이너에 대한 운영 체제를 지원하지 않는다.

브라우저에서 코드스페이스에 연결할 수 있습니다. {% 데이터 변수.product.prodname_vscode %}, JetBrains Gateway 애플리케이션에서 또는 {% 데이터 변수.product.prodname_cli %}를 사용하여 사용할 수 있습니다. 연결하면 도커 컨테이너 안에 배치됩니다. 외부 리눅스 가상 머신 호스트에 액세스할 수 없습니다.

![애저 가상 머신에서 실행되는 코드 편집기와 코드스페이스의 관계를 나타내는 다이어그램.](/assets/images/help/codespaces/codespaces-diagram.png)

## Benefits of {% data variables.product.prodname_github_codespaces %}

Reasons for choosing to work in a codespace include:

- **Use a preconfigured development environment** - You can work in a development environment that has been specifically configured for the repository. It will have all of the tools, languages, and configurations you need to work on that project. Everyone who works on that repository in a codespace will have the same environment. This reduces the likelihood of environment-related problems occurring and being difficult to debug. Each repository can have settings that will give contributors a ready-to-use, fit-for-purpose environment, and the environment on your local machine will be unchanged.
- **Access the resources you need** - Your local computer may not have the processing power, or storage space, you need to work on a project. {% data variables.product.prodname_github_codespaces %} allows you to work remotely on a machine with adequate resources.
- **Work anywhere** - All you need is a web browser. You can work in a codespace on your own computer, on a friend's laptop, or on a tablet. Open your codespace and pick up from where you left off on a different device.
- **Choose your editor** - Work in the browser in the {% data variables.product.prodname_vscode_shortname %} web client, or choose from a selection of desktop-based applications.
- **Work on multiple projects** - You can use multiple codespaces to work on separate projects, or on different branches of the same repository, compartmentalizing your work to avoid changes made for one piece of work accidentally affecting something else you're working on.
- **Pair program with a teammate** - If you work on a codespace in {% data variables.product.prodname_vscode_shortname %}, you can use Live Share to work collaboratively with other people on your team. For more information, see "[AUTOTITLE](/codespaces/developing-in-codespaces/working-collaboratively-in-a-codespace)."
- **Publish your web app from a codespace** - Forward a port from your codespace and then share the URL, to allow teammates to try out the changes you've made to the application before you submit those changes in a pull request.
- **Try out a framework** - {% data variables.product.prodname_github_codespaces %} reduces the setup time when you want to learn a new framework. Just create a codespace from one of the [quickstart templates](https://github.com/codespaces/templates).

## Using {% data variables.product.prodname_github_codespaces %}

To begin developing using cloud-based compute resources, you can create a codespace from a template or from any branch or commit in a repository. When you create a codespace from a template, you can start from a blank template or choose a template suitable for the work you're doing.

{% data reusables.codespaces.links-to-get-started %}

### Using codespaces owned by your personal account

All personal {% data variables.product.prodname_dotcom_the_website %} accounts have a monthly quota of free use of {% data variables.product.prodname_github_codespaces %} included in the Free or Pro plan. You can get started using {% data variables.product.prodname_github_codespaces %} on your personal account without changing any settings or providing payment details.

If you create a codespace from an organization-owned repository, use of the codespace will either be charged to the organization (if the organization is configured for this), or to your personal account.

{% data reusables.codespaces.codespaces-continue-by-paying %}

{% ifversion ghec %}
{% data reusables.codespaces.codespaces-unavailable-for-emus %}
{% endif %}

### Using organization-owned codespaces

Owners of organizations on {% data variables.product.prodname_team %} and {% data variables.product.prodname_enterprise %} plans can pay for their members' and collaborators' use of {% data variables.product.prodname_github_codespaces %}. This applies to codespaces created from repositories owned by the organization. For more information, see "[AUTOTITLE](/codespaces/managing-codespaces-for-your-organization/choosing-who-owns-and-pays-for-codespaces-in-your-organization)." You can set a spending limit for use of {% data variables.product.prodname_github_codespaces %} on your organization or enterprise account. For more information, see "[AUTOTITLE](/billing/managing-billing-for-github-codespaces/managing-the-spending-limit-for-github-codespaces)."

If use of a codespace will be billed to an organization or enterprise, this is shown when the codespace is created. For more information, see "[AUTOTITLE](/codespaces/developing-in-codespaces/creating-a-codespace-for-a-repository#creating-a-codespace-for-a-repository)." Codespaces that are billed to an organization, or its parent enterprise, are owned by the organization and can be deleted by an organization owner. For more information, see "[AUTOTITLE](/codespaces/developing-in-codespaces/deleting-a-codespace#deleting-codespaces-in-your-organization)."

{% data reusables.codespaces.when-you-can-create-codespaces %}

### Customizing {% data variables.product.prodname_github_codespaces %}

To customize the runtimes and tools in your codespace, you can create one or more dev container configurations for your repository. Adding dev container configurations to your repository allows you to define a choice of different development environments that are appropriate for the work people will do in your repository.

If you create a codespace from a repository without any dev container configurations, {% data variables.product.prodname_github_codespaces %} will clone your repository into an environment with the default codespace image that includes many tools, languages, and runtime environments. If you create a codespace from a template, you might start with some initial configuration on top of the default image. For more information, see "[AUTOTITLE](/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers)."

You can personalize aspects of your codespace environment by using a public [dotfiles](https://dotfiles.github.io/tutorials/) repository. You can use dotfiles to set shell aliases and preferences, or to install your personal preference of the tools you like to use. If you use {% data variables.product.prodname_github_codespaces %} in the browser, or in {% data variables.product.prodname_vscode %}, you can use [Settings Sync](https://code.visualstudio.com/docs/editor/settings-sync) to give your codespace editor the same settings, keyboard shortcuts, snippets, and extensions that you have set up in your local installation of {% data variables.product.prodname_vscode %}.

For more information, see "[AUTOTITLE](/codespaces/customizing-your-codespace)".

## Billing for {% data variables.product.prodname_codespaces %}

For information on pricing, storage, and usage for {% data variables.product.prodname_github_codespaces %}, see "[AUTOTITLE](/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces)."

{% data reusables.codespaces.codespaces-spending-limit-requirement %}

{% data reusables.codespaces.codespaces-monthly-billing %} For information on how organizations owners and billing managers can manage the spending limit for {% data variables.product.prodname_github_codespaces %} for an organization, see "[AUTOTITLE](/billing/managing-billing-for-github-codespaces/managing-the-spending-limit-for-github-codespaces)."
