sinlee7022@gmail.com
제목: 기본 커뮤니티 건강 파일 작성
도입부: 'CONTRIBUTING 및 CODE_OF_CONDUCT와 같은 기본 커뮤니티 건강 파일을 만들 수 있습니다. 기본 파일은 해당 유형의 자체 파일을 포함하지 않는 계정이 소유한 저장소에 사용될 것입니다.'
redirect_from:
  - /articles/reating-a-default-community-health-file-for-you-organization
  - /github/building-a-strong-community/reating-a-default-community-health-file-for-Your-organization
  - /github/building-a-strong-community/creating-a-default-community-health-file
버전:
 fpt: '*'
    게스: '    *'
   게크: ' *  게크: ' *'  
주제:
  -    공동체  
짧은 제목: 지역사회 건강 파일
---

##    기본 커뮤니티 건강 파일에 관한  

  기본 커뮤니티 건강 파일을 공용 저장소에 추가할 수 있습니다.    `.github`  , 저장소의 뿌리 또는 에    `의사`    또는    `.github`    폴더  

{% data variable.product.product_name %}는 다음 각 호의 어느 하나에 해당하는 곳에 해당 유형의 자체 파일이 없는 계정이 소유한 저장소에 기본 파일을 사용하고 표시합니다.
-    저장소근  
-   에   `.github`   폴더 
-   에   `의사`   폴더 

예를 들어 자체적으로 기여 파일이 없는 저장소에서 이슈를 생성하거나 요청을 당기는 사람은 기본 기여 파일에 대한 링크를 볼 수 있습니다. 저장소가 자체 파일을 가지고 있는 경우  `.github/ISSUE_TEMPLATE`  이슈 템플릿 또는 a를 포함하는 폴더 {% ifversion fpt 또는 ghes 또는 ghec %}  _config.yml_  파일,{% endif %} default의 내용은 하나도 없습니다  `.github/ISSUE_TEMPLATE`  폴더를 사용할 것입니다.

기본 파일은 개별 저장소의 클론, 패키지 또는 다운로드에만 포함되지 않습니다.  `.github`  저장소

##  지원 파일 유형

조직에서 기본값 {% ifversion fpt 또는 ghes 또는 ghec %} 또는 다음 지역사회 건강 파일에 대한 개인 계정 {% endif %}을 생성할 수 있습니다.

지역사회 건강 파일 | 설명
---|-{% ifversion fpt 또는 ghec %}
_CODE_OF_CONDUCT.md_  | CODE_OF_CONDUCT 파일은 커뮤니티에 참여하는 방법에 대한 표준을 정의합니다. 자세한 내용은 "를 참조하십시오.[자동제목].{% endif %}
_CONTRIBUTING.md_  | 기여 파일은 사람들이 당신의 프로젝트에 어떻게 기여해야 하는지를 전달합니다. 자세한 내용은 "를 참조하십시오.[자동제목](/지역사회/사회-기업-건강기여/기여-기관-기여).{% ifversion discussion-category-forms %}
토론 범주 형식 | 토론 범주 형식은 커뮤니티 구성원이 저장소에서 새로운 토론을 열 때 사용할 수 있는 템플릿을 사용자 정의합니다. 자세한 내용은 "를 참조하십시오.[자동제목](/토론/관리-토론-당신의 공동체를 위한/토론/창조-범주-형태).{% endif %}{% ifversion fpt 또는 ghec %}
_FUNDING.yml_ | FUNDING 파일은 오픈 소스 프로젝트에 대한 자금 지원 옵션의 가시성을 높이기 위해 저장소에 스폰서 버튼을 표시합니다. 자세한 내용은 "를 참조하십시오.[AUTOTITLE](/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/displaying-a-sponsor-button-in-your-repository).{% endif %}
_GOVERNANCE.md_ | A GOVERNANCE file lets people know about how your project is governed. For example, it might discuss project roles and how decisions are made.
Issue and pull request templates{% ifversion fpt or ghes or ghec %} and _config.yml_{% endif %} | Issue and pull request templates customize and standardize the information you'd like contributors to include when they open issues and pull requests in your repository. For more information, see "[AUTOTITLE](/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates)."{% ifversion fpt or ghes or ghec %}
`SECURITY.md` | A SECURITY file gives instructions for how to report a security vulnerability in your project. For more information, see "[AUTOTITLE](/code-security/getting-started/adding-a-security-policy-to-your-repository)."{% endif %}
_SUPPORT.md_ | A SUPPORT file lets people know about ways to get help with your project. For more information, see "[AUTOTITLE](/communities/setting-up-your-project-for-healthy-contributions/adding-support-resources-to-your-project)."

You cannot create a default license file. License files must be added to individual repositories so the file will be included when a project is cloned, packaged, or downloaded.

## Creating a repository for default files

{% data reusables.repositories.create_new %}
1. Use the **Owner** drop-down menu, and select the organization{% ifversion fpt or ghes or ghec %} or personal account{% endif %} you want to create default files for.
   ![Screenshot of the owner menu for a new {% data variables.product.prodname_dotcom %} repository. The menu shows two options, octocat and github.](/assets/images/help/repository/create-repository-owner.png)
1. In the "Repository name" field, type **.github**.
1. Optionally, in the "Description" field, type a description.
1. Make sure the repository status is set to **Public**. A repository for default files cannot be private.
{% data reusables.repositories.initialize-with-readme %}
{% data reusables.repositories.create-repo %}
1. In the repository, create one of the supported community health files. Issue templates{% ifversion fpt or ghes or ghec %} and their configuration file{% endif %} must be in a folder called `.github/ISSUE_TEMPLATE`. All other supported files may be in the root of the repository, the `.github` folder, or the `docs` folder. For more information, see "[AUTOTITLE](/repositories/working-with-files/managing-files/creating-new-files)."
