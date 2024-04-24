# node-module-import

개발에 필요한 노드 모듈을 Nexus(private repository)에 업로드 하기 위해선 **tgz**(tarball) 형식으로 압축해야 합니다.

본 프로젝트는 노드 모듈(의존 노드 모듈 포함)을 자동으로 tgz 형식으로 압축하기 위해 만들어졌습니다.

## Quick start

```bash
# 1. 준비
cd workspaces # 작업 공간으로 이동
git clone https://github.com/woori-fis/node-module-import.git # 프로젝트 클론
cd node-module-import # 프로젝트로 이동

# 2. 노드 모듈 설치
npm i ${node_module} # 필요한 노드 모듈 설치

# 3. 노드 모듈 압축
npm run start
```

프로젝트 루트 경로에 생성된 tarballs 폴더를 확인합니다.

$\color{red}주의사항$

이전에 작업한 이력은 반드시 삭제하고, Git에 반영하지 않습니다.

1. package.json의 dependencies 비워두기
2. 프로젝트 루트 경로에 node_modules 삭제하기
3. 프로젝트 루트 경로에 tarballs 삭제하기
4. package-lock.json 삭제하기

## Example

```bash
# 모듈 설치
npm i youtube-player @types/youtube-player
npm run start
```
