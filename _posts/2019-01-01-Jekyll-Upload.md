---
title: Github에 Jekyll 페이지 만들어보기
categories: [기타]
tags: [github, jekyll]
published: true
---

### 공식 사이트
- https://jekyllrb.com/

### 올려보자
1) git repository 를 하나 만든다
    (git repository 를 만들때 **id.github.io로 만들면 id.github.io 로 접속이 가능**)

2) 뭐라도 올린다 (readme.md 라던가)

3) settings - GitHub Pages - Source - 뭐든 선택 (나는 master branch) - save
    - **(생성에 약 30분 정도 걸린다.)**

4) settings - Github Pages - Theme Chooser 에서 Jekyll 테마를 고르면 된다.

5) 사람들이 만들어놓은 Jekll 테마를 사용하려면 http://jekyllthemes.org/ 에서 가져온다.
    - 본인 계정으로 git clone 하거나 / 다운받아서 repository 에 올리거나 ...

6) theme 는 [minimal mistakes](https://github.com/mmistakes/minimal-mistakes) 를 활용, _config.yml 을 설정한다.

7) _config.yml은 https://github.com/mmistakes/minimal-mistakes/blob/master/_config.yml 을 복사해서 활용
    - remote_theme 를 활용 (theme 아니고)
    - title, locale, name, masthead_title 등등 필요한 것들을 세팅한다.
    - index.html / index.md 를 만든다 (https://github.com/mmistakes/minimal-mistakes/blob/master/index.html 참고)
    - _data/navigation.yml 을 만든다 (https://github.com/mmistakes/minimal-mistakes/blob/master/_data/navigation.yml 참고)

### 기능 확장하기
1) 댓글 기능
    - [디스커스](https://www.google.com/search?q=disqus&oq=disqus&aqs=chrome..69i57j0j69i60l3j0.1373j0j7&sourceid=chrome&ie=UTF-8) 사이트 추가해서 short name 알아내고 _config.yml 에 comments 를 disqus 로 세팅하고 숏네임을 세팅하면 끝

2) 상단 카테고리 / 태그 등 기능 페이지 만들기
    - _pages/category_archive.md , _pages/tag_archive.md 등을 역시 위에 참고한 주소에서 복사해서 붙여넣는다.

3) 검색 기능 - _config.yml 에서 search: true 세팅한다

### 글 쓰기

_post/ 아래에 YYYY-MM-DD-제목.md 파일을 만든다.

```
---
layout: post
title: 제목
categories: [ios, swift]
tags: [tag1, tag2]
published: true
---
글 내용
글 내용
```
과 같이 글을 입력한다.


### 추가 해야 할 일 / 하고 싶은 일
- [ ] 태그 클라우드 사이드바 추가하기 (잘 안됨...)
- [ ] 글 쉽게 쓰기, github 페이지에서 바로 쓰기보다 편한. 뭔가 툴이 있으면 좋겠다. 아니면 만들어볼까


### 지식 정리
- githubID.github.io 로 repository 이름을 지으면 http://githubID.github.io 로 접속 가능한 페이지를 얻을 수 있음
    - (그외 repository 이름은 http://githubID.github.io/repositoryName 이 됨)
- private repository 는 GitHub Pages 가 안된다.
- GitHub Pro / Team / Enterprise 는 private repository 도 github page 가능 (github pro 는 월 7달러!)

### hexo vs jekyll
- https://qvil.github.io/blog/why-jekyll/
- https://stackshare.io/stackups/hexo-vs-jekyll

### Ref.
- 공식 사이트
    - https://jekyllrb-ko.github.io/
    - https://help.github.com/categories/github-pages-basics/ - github 페이지 help page
    - https://help.github.com/articles/configuring-jekyll/ - github jekyll 설정

- 다른 사람들의 세팅 이야기
    - https://dreamgonfly.github.io/2018/01/27/jekyll-remote-theme.html
        (Ref. https://github.com/dreamgonfly/dreamgonfly.github.io)
    - https://github.com/gjchoi/gjchoi.github.io/blob/master/_posts/2016-02-18-Github-page%EB%A1%9C-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0.md
    - http://labs.brandi.co.kr/2018/05/14/chunbs.html
    - [카카오 기술 블로그 Jekyll 사용](http://tech.kakao.com/2016/07/07/tech-blog-story/)

- 테마
    - https://github.com/mmistakes/minimal-mistakes - 선택한 테마
        - https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/ - 설정방법
    - https://isme2n.github.io/devlog/2017/03/09/Blog-Jekyll-theme/ - 추천 테마
