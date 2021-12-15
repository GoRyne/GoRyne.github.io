# How i build github.io
1. ruby환경 세팅
2. jekyll 설치
3. theme 적용
4. 댓글창
5. favicon 추가
6. **[GoRyne's blog](https://goryne.github.io/)**

</br></br>
## Ruby 환경 세팅
Jekyll을 사용하기 위해선 ruby 환경을 먼저 셋팅해야 하며 윈도우 사용자의 경우엔 루비 인스톨러가 선행적으로 설치 되어야 한다.

**[루비 인스톨러 링크](https://rubyinstaller.org/downloads/)** </br>
**[루비 다운로드 링크](https://www.ruby-lang.org/ko/downloads/)**

</br></br>
## Jekyll 설치
루비가 정상적으로 설치 되었다면 지킬은 아래의 명령어로 쉽게 설치 가능하다</br>
`gem install jekyll bundler`</br></br>

github.io 레포지토리에서 `jekyll new . --force` 명령어를 통해서 기본 틀을 만들 수 있으며 정상적으로 만들어졌는지 확인하기 위해 `jekyll serve` 명령어를
사용하면 된다. </br></br>

`C:/Ruby30-x64/lib/ruby/gems/3.0.0/gems/jekyll-4.2.0/lib/jekyll/commands/serve/servlet.rb:3:in require: cannot load such file -- webrick (LoadError)`
이런 오류가 발생했을 땐  `bundle add webrick' 명령어를 사용하면 된다.

</br></br>
## Theme 적용
테마를 적용하기 위해선 먼저 **[여기](https://jekyll-themes.com/free/)** 와 같은 jekyll 테마를 모아둔 곳에서 원하는 테마를 선택한 후 그대로 github.io에 덮어쓰거나
원하는 테마를 선택한 후 로컬에 다운로드 받은 후 다운로드 받은 파일을 github.io 레포지토리에 덮어쓰면 된다.</br></br>
테마를 적용한 후 css에러가 나왔다면 `_config.yml` 파일에서  `baseurl` 과 `url`이 정상적인 위치를 가리키고 있는지 확인한다.
만약 건드리기 전이라면 `url: username.github.io` 형식으로 바꿔주면 정상적으로 작동된다.

</br></br>
## 댓글창 
댓글창을 위해서 **[disqus](https://disqus.com)** 의 기능을 이용하였다. 
</br>
</br>
먼저 **[disqus](https://disqus.com)** 를 누르면 링크로 이동하게 된다.
</br>
</br>
disqus 회원가입 후 플랫폼에 jekyll을 선택하고 추가 설정을 해준다.
</br>
설정을 마친 후 `_config.yml` 파일에 
</br>
```
comment:
  provider: "disqus"
  disqus:
    shortname: "본인이 disqus에서설정한 이름"
```
해당 코드를 추가해 준다</br></br>

이후 disqus에서 아무런 플랫폼을 선택하지 않았을 때 나오는 Universal code를 `_layout/post.html` 파일에 원하는 위치에 추가해준다
</br></br>
여기까지 끝났다면 앞으로 댓글기능이 달리길 원하는 post에 `comments: true` 를 적어주면 끝난다.


</br></br>
## Favicon 추가
favicon으로 쓸 이미지를 파일로 저장하고 **[여기](https://www.favicon-generator.org/)** 에서 해당 이미지를 .ico 형식으로 바꿔준다
</br></br>
이후 `본인의 문서가 정의된 html 파일` 에서 `<link rel="icon" type="image/png" href="ico경로">` 를 적어주면 끝난다. 




</br></br></br></br>
## 혹시라도 jekyll 테마에 관해서 궁금증이 있으시다면 밑을 참고해주세요!

</br></br>
# [Start Bootstrap - Clean Blog Jekyll](https://startbootstrap.com/themes/clean-blog-jekyll/) - Official Jekyll Version

[Clean Blog Jekyll](https://startbootstrap.com/themes/clean-blog-jekyll/) is a stylish, responsive blog theme for [Bootstrap](https://getbootstrap.com/) created by [Start Bootstrap](https://startbootstrap.com/). This theme features a blog homepage, about page, contact page, and an example post page along with a working contact form powered by [Formspree](https://formspree.io/).

This repository holds the official Jekyll version of the Clean Blog theme on Start Bootstrap!


## Bugs and Issues

Have a bug or an issue with this template? [Open a new issue](https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll/issues) here on GitHub!

## About

Start Bootstrap is an open source library of free Bootstrap templates and themes. All of the free templates and themes on Start Bootstrap are released under the MIT license, which means you can use them for any purpose, even for commercial projects.

* <https://startbootstrap.com>
* <https://twitter.com/SBootstrap>

Start Bootstrap was created by and is maintained by **[David Miller](http://davidmiller.io/)**.

* <http://davidmiller.io>
* <https://twitter.com/davidmillerhere>
* <https://github.com/davidtmiller>

Start Bootstrap is based on the [Bootstrap](https://getbootstrap.com/) framework created by [Mark Otto](https://twitter.com/mdo) and [Jacob Thorton](https://twitter.com/fat).

## Copyright and License

Copyright 2013-2021 Start Bootstrap LLC. Code released under the [MIT](https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll/blob/master/LICENSE) license.
