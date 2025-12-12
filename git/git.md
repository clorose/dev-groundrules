# Git Commit Rules

커밋 메시지를 쓸 때 내가 지키는 규칙들을 정리한 문서입니다.

- 기본 구조: **Conventional Commit** 타입  
- 보조 표기: **Gitmoji**  
- 상태/기분 로그: **Commit Mood (커스텀 이모지 + 태그)**

---

## 1. Conventional Commit 타입

가장 기본이 되는 커밋 타입 규칙입니다. 타입은 영어로, 메시지는 자유롭게 (한글/영문) 사용합니다.

### 기본 포맷 (기본값)

```
<gitmoji><type>: <subject>
```

markdown
코드 복사

- `<type>`: Conventional Commit 타입 (영문, 소문자)
- `<subject>`:
  - 50자 이내
  - 마침표(`.`) 금지
  - 동사로 시작 (add / update / remove / fix 등)
  - 한글/영문 자유


### 📘 Conventional Commit 타입 총정리표 (핵심 + 확장)

| 타입         | 의미                                    | 예시                                     |
| ------------ | --------------------------------------- | ---------------------------------------- |
| **feat**     | 새로운 기능 추가                        | `feat: add search bar`                   |
| **fix**      | 버그 수정                               | `fix: resolve null pointer`              |
| **docs**     | 문서 변경                               | `docs: update README`                    |
| **style**    | 의미 없는 스타일 변경(포맷/세미콜론 등) | `style: apply prettier`                  |
| **refactor** | 기능 변화 없는 구조 개선                | `refactor: extract utils`                |
| **perf**     | 성능 개선                               | `perf: optimize image resize`            |
| **test**     | 테스트 추가/수정                        | `test: add login tests`                  |
| **build**    | 빌드 시스템 변경(Dockerfile 포함)       | `build: update Dockerfile base image`    |
| **ci**       | CI/CD 설정 변경                         | `ci: update GitHub Actions node version` |
| **config**   | 설정 파일 변경                          | `config: update eslint rules`            |
| **chore**    | 잡일(Deps 업데이트 포함)                | `chore: bump react to 18`                |
| **revert**   | 이전 커밋 되돌림                        | `revert: revert hotfix`                  |

---

| 타입        | 의미                            | 예시                                     |
| ----------- | ------------------------------- | ---------------------------------------- |
| **db**      | DB 스키마/마이그레이션          | `db: add users table migration`          |
| **api**     | API 스펙/엔드포인트 변경        | `api: update /auth/login response shape` |
| **logging** | 로깅 시스템 개선                | `logging: add request trace id`          |
| **merge**   | 브랜치 병합                     | `merge: merge feature/auth into main`    |
| **wip**     | 작업 진행 중 (Work In Progress) | `wip: working on sidebar refactor`       |

---

## 2. Gitmoji 가이드

커밋 타입과 함께 붙여서 쓰는 Gitmoji 목록이다.  
의미가 겹치지 않도록, 이 표 기준으로만 사용.

| 이모지 | 코드                          | 설명                                             |
| ------ | ----------------------------- | ------------------------------------------------ |
| 🎨      | `:art:`                       | 코드 구조 / 포맷을 개선할 때                     |
| ⚡️      | `:zap:`                       | 성능을 개선할 때                                 |
| 🔥      | `:fire:`                      | 코드나 파일을 삭제할 때                          |
| 🐛      | `:bug:`                       | 버그를 수정할 때                                 |
| 🚑️      | `:ambulance:`                 | 긴급 핫픽스                                      |
| ✨      | `:sparkles:`                  | 새로운 기능을 추가할 때                          |
| 📝      | `:memo:`                      | 문서를 추가하거나 수정할 때                      |
| 🚀      | `:rocket:`                    | 배포 관련 작업                                   |
| 💄      | `:lipstick:`                  | UI / 스타일 파일을 추가·수정할 때                |
| 🎉      | `:tada:`                      | 프로젝트를 시작할 때                             |
| ✅      | `:white_check_mark:`          | 테스트를 추가/수정/통과시켰을 때                 |
| 🔒️      | `:lock:`                      | 보안 / 프라이버시 이슈를 수정할 때               |
| 🔐      | `:closed_lock_with_key:`      | 시크릿을 추가하거나 업데이트할 때                |
| 🔖      | `:bookmark:`                  | 릴리즈 / 버전 태그                               |
| 🚨      | `:rotating_light:`            | 컴파일러 / 린터 경고를 수정할 때                 |
| 🚧      | `:construction:`              | 작업 진행 중(WIP)                                |
| 💚      | `:green_heart:`               | CI 빌드를 고쳤을 때                              |
| ⬇️      | `:arrow_down:`                | 의존성을 다운그레이드할 때                       |
| ⬆️      | `:arrow_up:`                  | 의존성을 업그레이드할 때                         |
| 📌      | `:pushpin:`                   | 의존성 버전을 고정할 때                          |
| 👷      | `:construction_worker:`       | CI 빌드 시스템을 추가·수정할 때                  |
| 📈      | `:chart_with_upwards_trend:`  | 분석/트래킹 코드를 추가·수정할 때                |
| ♻️      | `:recycle:`                   | 리팩터링                                         |
| ➕      | `:heavy_plus_sign:`           | 의존성을 추가할 때                               |
| ➖      | `:heavy_minus_sign:`          | 의존성을 제거할 때                               |
| 🔧      | `:wrench:`                    | 설정 파일을 추가·수정할 때                       |
| 🔨      | `:hammer:`                    | 개발 스크립트를 추가·수정할 때                   |
| 🌐      | `:globe_with_meridians:`      | i18n / L10n (다국어/현지화) 작업                 |
| ✏️      | `:pencil2:`                   | 오타 수정                                        |
| 💩      | `:poop:`                      | 나쁜 코드(나중에 개선해야 할 코드)를 작성했을 때 |
| ⏪️      | `:rewind:`                    | 변경 사항을 되돌릴 때                            |
| 🔀      | `:twisted_rightwards_arrows:` | 브랜치를 머지할 때                               |
| 📦️      | `:package:`                   | 빌드 산출물/패키지를 추가·수정할 때              |
| 👽️      | `:alien:`                     | 외부 API 변경 때문에 코드를 수정할 때            |
| 🚚      | `:truck:`                     | 파일/경로/라우트 등을 이동하거나 이름을 바꿀 때  |
| 📄      | `:page_facing_up:`            | 라이선스를 추가·수정할 때                        |
| 💥      | `:boom:`                      | 호환이 깨지는 변경(Breaking change)을 추가할 때  |
| 🍱      | `:bento:`                     | 에셋(이미지 등)을 추가·수정할 때                 |
| ♿️      | `:wheelchair:`                | 접근성을 개선할 때                               |
| 💡      | `:bulb:`                      | 소스 코드에 주석을 추가·수정할 때                |
| 🍻      | `:beers:`                     | 술 마시고 코딩했을 때(장난/밈용)                 |
| 💬      | `:speech_balloon:`            | 텍스트·문구를 추가·수정할 때                     |
| 🗃️      | `:card_file_box:`             | DB 관련 변경을 할 때                             |
| 🔊      | `:loud_sound:`                | 로그를 추가·수정할 때                            |
| 🔇      | `:mute:`                      | 로그를 제거할 때                                 |
| 👥      | `:busts_in_silhouette:`       | 기여자 정보를 추가·수정할 때                     |
| 🚸      | `:children_crossing:`         | UX / 사용성을 개선할 때                          |
| 🏗️      | `:building_construction:`     | 아키텍처를 변경할 때                             |
| 📱      | `:iphone:`                    | 반응형 디자인 작업                               |
| 🤡      | `:clown_face:`                | 목(mock) 객체/코드를 추가·수정할 때              |
| 🥚      | `:egg:`                       | 이스터에그를 추가·수정할 때                      |
| 🙈      | `:see_no_evil:`               | `.gitignore`를 추가·수정할 때                    |
| 📸      | `:camera_flash:`              | 스냅샷을 추가·수정할 때                          |
| ⚗️      | `:alembic:`                   | 실험용 코드 / 실험 수행                          |
| 🔍️      | `:mag:`                       | SEO 개선                                         |
| 🏷️      | `:label:`                     | 타입을 추가·수정할 때                            |
| 🌱      | `:seedling:`                  | 시드(seed) 데이터를 추가·수정할 때               |
| 🚩      | `:triangular_flag_on_post:`   | 기능 플래그를 추가·수정·삭제할 때                |
| 🥅      | `:goal_net:`                  | 에러를 캐치하는 코드 추가·수정                   |
| 💫      | `:dizzy:`                     | 애니메이션/트랜지션을 추가·수정할 때             |
| 🗑️      | `:wastebasket:`               | 나중에 지울 예정인 코드에 폐기(deprecate) 표시   |
| 🛂      | `:passport_control:`          | 권한/역할/퍼미션 관련 코드를 작업할 때           |
| 🩹      | `:adhesive_bandage:`          | 치명적이지 않은 간단한 이슈를 고칠 때            |
| 🧐      | `:monocle_face:`              | 데이터 탐색 / 인스펙션                           |
| ⚰️      | `:coffin:`                    | 사용되지 않는(dead) 코드를 제거할 때             |
| 🧪      | `:test_tube:`                 | 실패하는 테스트를 추가할 때                      |
| 👔      | `:necktie:`                   | 비즈니스 로직을 추가·수정할 때                   |
| 🩺      | `:stethoscope:`               | 헬스체크(healthcheck)를 추가·수정할 때           |
| 🧱      | `:bricks:`                    | 인프라 관련 변경                                 |
| 🧑‍💻      | `:technologist:`              | 개발자 경험(DX)을 개선할 때                      |
| 💸      | `:money_with_wings:`          | 후원/결제/돈 관련 인프라를 추가·수정할 때        |
| 🧵      | `:thread:`                    | 멀티스레딩/동시성 관련 코드를 추가·수정할 때     |
| 🦺      | `:safety_vest:`               | 검증/validation 관련 코드를 추가·수정할 때       |
| ✈️      | `:airplane:`                  | 오프라인 지원을 개선할 때                        |
| 🦖      | `:t-rex:`                     | 하위 호환성을 추가하는 코드                      |

---

## 3. Commit Mood (옵션)

> 기본 타입(feat/fix/...) 뒤에 이모지 + 태그를 붙여서 기분/상태를 남기는 용도.  
> 예) `feat: add settings panel 🥱 [zzz]`

| #   | 카테고리            | 이모지 | 태그       | 설명                                            |
| --- | ------------------- | ------ | ---------- | ----------------------------------------------- |
| 1   | 거의 안함           | 🥱      | `zzz`      | 거의 안 함. README/주석 한 줄 정도만 수정한 날  |
| 2   | 안 해도 상관 없었음 | 🕰️      | `waste`    | 굳이 안 해도 됐던, 의미 낮은 변경               |
| 3   | 심심해서 함         | 🎮      | `fun`      | 심심해서 만지작한 변경. 그래도 코드는 정상 동작 |
| 4   | 그냥 읽기만 함      | 👁️‍🗨️      | `looking`  | 코드/문서 읽고 훑어본 날. 메모 조금 남긴 정도   |
| 5   | 아이디어 정리       | 🧠      | `ideas`    | 아이디어, TODO, 구상만 정리한 커밋              |
| 6   | 정리만 함           | 🧹      | `clean`    | 포맷팅, import 정리, 파일/폴더 정리 위주        |
| 7   | 설정만 만짐         | 🛠️      | `settings` | dotfiles·툴 설정·옵션만 손댄 날                 |
| 8   | 조금만 함           | 🐾      | `tiny`     | 아주 작은 수정/개선 한두 개만 한 날             |
| 9   | 기분 좋음           | 🤗      | `happy`    | 사소하지만 본인 기준 꽤 만족스러운 변경         |
| 10  | 느려짐              | 🐢      | `turtle`   | 튜닝했는데 체감상 더 느려짐. 그래도 돌아는 감   |
| 11  | 걍 자러갈래 ㅡㅡ    | 🛏      | `sleep`    | 오늘 한 건 애매하지만 여기까지 저장하고 끝      |
| 12  | 멘탈 나감 (“안해!”) | 😡      | `altf4`    | 멘탈 터진 상태에서 마무리 커밋. 빌드는 됨       |
