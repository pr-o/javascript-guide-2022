# NVM (0.39.1)

Node.js 버전 매니저의 약자로 NVM이라고 불리는 커맨드라인 툴입니다. 다음과 같이 서로 다른 코드베이스들이 각각 다른 Node.js 버전을 사용하는 상황에서 생길 수 있는 혼선을 줄일 수 있습니다:

{% hint style="info" %}
예시

> **S**는 동료 **A** 그리고 동료 **B**의 프로젝트에 협업자로 참여해 도와주기로 했습니다. 평일에는 A와 협업하고 주말에는 B와 협업할 예정입니다. 그런데 S의 환경엔 16.16.0 버전의 Node.js가 설치되어있는 반면, A의 프로젝트는 12.20.0 버전을, B의 프로젝트는 14.19.0 버전을 사용하고 있습니다. 필요할때마다 Node.js를 재설치해야할까요?
{% endhint %}



터미널에서 다음 명령어를 실행하면 NVM설치 스크립트를 다운받아 실행합니다.

```bash
curl -o- <https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh> | bash
```



이 스크립트는 설치 마지막 단계에서 다음의 코드 두 줄을 프로파일 파일의(`~/.bash_profile`, `~/.zshrc`, `~/.profile`, 혹은 `~/.bashrc`) 최하단에 덧붙이도록 되어있지만 권한 문제로 파일 수정에 실패하는 경우가 있어 이를 확인할 필요가 있습니다.

```bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \\. "$NVM_DIR/nvm.sh" # This loads nvm
```



사용하는 shell(터미널)의 유형에 따라 어떤 이름의 프로파일 파일을 사용하는지 다를 수 있습니다. 아래 커맨드를 실행하면 어떤 프로파일 파일(들)을 사용하고 있는지 알아볼 수 있습니다.

```bash
ls -alp ~ | grep -v /
```



아래 스크린샷에 보이는 것처럼 저의 경우에는 언급한 네개의 파일들 중 `.zshrc` 파일이 유일한 프로파일 파일로 존재하고 있는 것을 확인할 수 있습니다. 이 파일을 텍스트 에디터로 열어 위의 두줄짜리 코드가 파일의 최하단에 적혀있는지 확인하고, 그렇지 않다면 직접 붙여넣고 저장해주세요.

![](<../.gitbook/assets/Screen Shot 2022-07-23 at 1.51.29 PM.png>)

새로운 터미널 창을 열고 다음 명령어를 실행해서 NVM이 잘 설치되었는지 확인합니다. `0.39.1` 처럼 설치한 버전의 정보가 출력된다면 설치를 성공적으로 마친 것입니다.

```bash
nvm -v
```



설치한 NVM을 사용해 특정 Node.js 버전을 설치하기 위해서는 다음 명령어를 사용하면 됩니다.

```bash
nvm install 16.16.0    # nvm install <version>
```



이렇게 NVM을 통해 설치한 Node.js 버전은 기존에 내 환경에 설치했던 것과 별도로 설치되어, 다음과 같이 언제든지 바꿔 사용할 수 있습니다.

```bash
nvm use 16.16.0    # nvm use <version>
```



NVM을 사용해 버전을 오가다 보면 현재 어떤 버전을 쓰고 있는지 혼란이 올 수도 있는데, 그럴 때엔 다음 명령어로 현재 사용중인 Node.js 버전을 확인할 수 있습니다.

```bash
nvm current
```



이제 위에 들었던 예시와 같은 상황에 놓이더라도 문제 없습니다. A의 프로젝트 그리고 B의 프로젝트 작업 직전에 각각 `nvm use 12.20.0`, `nvm use 14.19.0` 명령어를 사용해 버전을 쉽게 오갈 수 있는데다가 제 로컬 환경과의 충돌도 피할 수 있기 때문이죠.

