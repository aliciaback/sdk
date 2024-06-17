# 시작하기 

## 옵션 1: 로컬 환경(리눅스, 맥OS, WSL이 설치된 윈도우)

> WSL이 설치된 윈도우를 사용하는 경우, 도커 데스크탑에서 WSL과의 통합을 활성화시키는 것을 잊지 마세요. 

[WSL이 설치된 윈도우 사용하는 방법](./windows-wsl.md)

### 요건 

컴퓨터에 다음 도구들이 설치되어 있어야 합니다. 

- Node.js 18+
- Docker 그리고 Docker Compose
- [jq](https://jqlang.github.io/jq/) 그리고 [yq](https://github.com/mikefarah/yq)

### 1. 갈라체인 CLI 설치 

```
npm i -g @gala-chain/cli
```

CLI 확인하기:

```
galachain --help
```

### 2. 프로젝트 초기 설정

```
galachain init <project-name>
```

`<project-name>` 디렉토리 내에 샘플 프로젝트가 생성됩니다.

모든 dependencies 설치:

```
npm i
```

### 3. 네트워크 시작 

```
npm run network:start
```

네트워크는 hot-reload/watch 모드에서 시작됩니다. 그러니 로그 프롬프트가 돌아가도록 그대로 두고, 새로운 프롬프트에서 아래 명령어를 실행합니다.

### 4. 통합 테스트 실행 

아래 명령어로 통합 테스트를 실행할 수 있습니다. 

```
npm run test:e2e
```

### 5. 블록 브라우저와 GraphQL에서 변경사항 확인하기

[http://localhost:3010/blocks](http://localhost:3010/blocks)로 이동하여 블록 브라우저를 확인합니다. 여기서는 여러분의 로컬 갈라체인 네트워크에 무엇이 저장되어 있는지 확인할 수 있습니다. 

[http://localhost:3010/graphiql](http://localhost:3010/graphiql)로 이동하여 GraphQL과 상호작용하고 쿼리를 실행합니다. 


### 6. 다음 단계 

- [체인코드 이터레이션](chaincode-development.md)
- [갈라체인 SDK에 익숙해지기](galachain.md)
- [gc-testnet로 체인코드 디플로이](chaincode-deployment.md)

---

## 옵션 2: 도커 이미지 사용(리눅스, 맥OS, 윈도우)

### 요건 

- 도커 데스크탑 또는 도커 CLI.
- [선택사항] [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) 확장 프로그램을 이용한 VSCode 

### 1. 도커 이미지 실행

```
docker run --privileged -d -p 3010:3010 -it --name <container_name> ghcr.io/galachain/sdk:latest
```

컨테이너가 실행 중인지 확인합니다.
도커 이미지는 새로운 프로젝트를 초기에 설정할 때 `chaincode-template`라는 이름을 디폴트로 설정합니다. 

### 2. 운영 중인 컨테이너 오픈하기 

#### 2.1 bash로 열기 

```
docker exec -ti <container_name> /bin/bash
```

#### 2.2 VSCode로 열기 (VSCode 및 Dev Containers 확장 프로그램 필요) 

VSCode를 열고 F1을 클릭하여 명령어 팔레트(Command Palette)를 엽니다. 그런 다음 `Dev Containers: Attach to Running Container`를 검색합니다. 

컨테이너를 연결한 후 프로젝트 폴더를 수동으로 열어야 할 수도 있습니다.

### 3. 네트워크 시작 

터미널이 열리면, 아래 명령어로 네트워크를 시작합니다. 

```
npm run network:start
```

네트워크는 개발 모드에서 시작되며, 로그를 표시하는 프롬프트는 남아 있습니다. 해당 프롬프트를 닫지 말고, 새로운 프롬프트를 열어 다음 명령어들을 계속 실행합니다. 

### 4. 통합 테스트 실행

이제 아래 명령어를 이용하여 통합 테스트를 수행할 수 있습니다. 

```
npm run test:e2e
```

### 5. 블록 브라우저와 GraphQL에서 변경사항 확인하기

[http://localhost:3010/blocks](http://localhost:3010/blocks)로 이동하여 블록 브라우저를 확인합니다. 여기서는 여러분의 로컬 갈라체인 네트워크에 무엇이 저장되어 있는지 확인할 수 있습니다.

[http://localhost:3010/graphiql](http://localhost:3010/graphiql)로 이동하여 GraphQL과 상호작용하고 쿼리를 실행합니다.

---

## 옵션 3: Dev Containers 사용(리눅스 또는 맥OS)

### 요건 

- [VSCode](https://code.visualstudio.com/)
- [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- Node.js
- 도커 

### 1. 갈라체인 CLI 설치

```
npm i -g @gala-games/chain-cli
```

CLI 확인하기:

```
galachain --help
```

### 2. 프로젝트 초기 설정 

```
galachain init <project-name>
```

`<project-name>` 디렉토리 내에 샘플 프로젝트가 생성됩니다.

VSCode에서 디렉토리를 엽니다. 

```
cd <project-name>
code .
```

### 3. Dev Container에서 열기 

VSCode에서 F1을 클릭하여 명령어 팔레트(Command Palette)를 엽니다. 그런 다음 `Dev Containers: Reopen in Container`를 검색합니다. 

![remote-command-palette](./assets/remote-command-palette.png)

상태 표시줄의 Remote Indicator를 클릭하면 가장 일반적인 명령어 목록을 확인할 수 있습니다. 

![remote-command-palette](./assets/remote-dev-status-bar.png)

### 4. Dependencies 설치 및 네트워크 시작 

Dev Container에서 새로운 프롬프트를 열고 아래 명령어를 실행합니다. 

```
npm install
```

```
npm run network:start
```

네트워크는 개발 모드에서 시작되기 때문에, 로그를 표시하는 프롬프트는 닫지 말고, 새로운 프롬프트를 열어 다음 명령어들을 실행합니다. 

### 5. 통합 테스트 실행 

이제 아래 명령어를 이용하여 통합 테스트를 수행할 수 있습니다.

```
npm run test:e2e
```

### 6. 블록 브라우저와 GraphQL에서 변경사항 확인하기 

[http://localhost:3010/blocks](http://localhost:3010/blocks)로 이동하여 블록 브라우저를 확인합니다. 여기서는 여러분의 로컬 갈라체인 네트워크에 무엇이 저장되어 있는지 확인할 수 있습니다.

[http://localhost:3010/graphiql](http://localhost:3010/graphiql)로 이동하여 GraphQL과 상호작용하고 쿼리를 실행합니다.

---

# 트러블슈팅 

## 윈도우 도커 데스크탑 

#### WSL이 설치된 윈도우를 사용하는 경우, 도커 데스크탑에서 WSL 통합을 활성화하는 것을 잊지 마세요.

```
Docker Desktop > Settins > Resources > WSL Integration
```

#### Docker: "image operating system "linux" cannot be used on this platform"(이미지 운영 체제 리눅스는 이 플랫폼에서 사용할 수 없음): "operating system is not supported."(운영체제 미지원)

윈도우 도커 데스크탑의 일부 버전은 버그로 인해 리눅스 이미지를 사용할 수 없습니다. 이러한 문제가 발생하는 경우, WSL2 백엔드를 이용하여 도커를 실행할 수 있습니다. 이를 위해서는 Docker Desktop > Settings > General에서 WSL2를 디폴트 백엔드로 설정하세요. 

#### Docker: "no matching manifest for windows/amd64 in the manifest list entries"(매니페스트 리스트에 윈도우/amd64와 일치하는 매니페스트 없음)

이 문제를 우회하려면 Docker daemon을 실험 모드에서 실행해 볼 수 있습니다. 

```
Docker Desktop > Settings > Docker Engine > Edit the Docker daemon file > Set the "experimental": true > Apply & Restart
```

## 도커 

#### Docker: Error response from daemon: Conflict. The container name "/<container_name>" is already in use by container "<container_id>".(해당 컨테이너 이름은 이미 다른 컨테이너가 사용하고 있음)

위와 같은 에러 메시지가 뜨는 경우, 해당 이름을 이미 사용하고 있는 컨테이너가 있다는 의미로, 해당 컨테이너를 삭제하거나 이름을 변경해야 합니다.

## WSL

#### ./fablo-target/fabric-config/configtx.yaml: no such file or directory

위와 같은 에러 메시지가 뜨는 경우, cmd 또는 powershell을 관리자(administrator)로서 실행하고 있는지 확인하세요. 

#### docker: Got permission denied

npm run network:start 또는 npm run network:up을 실행할 때 위와 같은 에러 메시지가 뜨는 경우, 다음과 같이 구성을 활성화합니다. `Settings` > `Resources` > `Expose daemon on tcp://localhost:2375 without TLS`.
