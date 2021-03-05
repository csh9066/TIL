# Git Flow

## 사용되는 브랜치

### master

- 실제 제품으로 출시 할 수 있는 브랜치
- 개발자가 직접 master 브랜치의 코드를 변경하고 commit 해서 안됨
- merge가 되면 태그에 버전 정보를 삽입

### develop

- 개발 중인 코드의 중심이 되는 브랜치
- master와 마찬가지로 코드를 변경하고 commit 해선 안되고 feature 브랜치를 기능을 추가하고 수정하고 merge해야 함

### feature

- develop 브랜치에서 파생된 브랜치로 실제 개발자가 개발을 브랜치
- 단위 기능별로 개발하고 개발이 완료되면 보통 pull request를 통해 코드리뷰를 받고 develop 브랜치에 merge함

### release

- 배포 전 (master브랜치에 merger 전)에 품질 테스트를 하기 위한 브랜치
- 버그 수정과 관련된 commit만을 실시한다
- 절때 기능변경, 사양변경 과 같은 commit을 하지 않는다

### hotfix

- 현재 출시되어 있는 master 브랜치에 버그가 발생됐을 때 긴급히 수정하는 브랜치
