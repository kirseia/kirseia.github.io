---
title: SwiftFormat 사용해보기
categories: [ios, swift]
tags: [swift, swiftFormat]
published: true
---
### 간단설명
swift 작성 된 코드의 formatting 을 수정해주는 툴

### 설치
```bash
$brew isntall swiftformat
```

### 사용

간단 사용 예

```bash
$swiftformat .
```

swift version 지정하기

```bash
$swiftformat --swiftversion 4.2 .
```

- build phase 시점에 넣어서 사용 가능 - 'Run Script build phase'

### 느낌?

- 아무 옵션 없이 한번 돌려봄 (기본 상태))
- 쓸데없는 변수 없애줌
- self. 없어도 되는 것 없애줌
- 사용하지 않는 변수 _ 로 대체
- 생각보다 느낌 좋음. 괜찮음. 도입할만함
- swiftlint 적용하고 있는 것과 상충하는 것들이 있긴 함. 옵션 조정 필요

### 나만의 룰 만들기

- .swiftformat 만들어서 정리하기

```
--header strip
--indentcase true
--wraparguments preserve
--wrapcollections before-first
--disable blankLinesAroundMark, ranges, spaceAroundParens, unusedArguments, emptyBraces, trailingCommas
--exclude Pods,Generated
```

### Ref.
- https://github.com/nicklockwood/SwiftFormat
