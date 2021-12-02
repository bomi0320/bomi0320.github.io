### build 과정

1. 아래 사이트에서 마음에 드는 깃허브 블로그 테마를 선택한다.

[github theme site](http://jekyllthemes.org/)

![pic1](/assets/img/readme1.PNG)



2. Homepage 버튼을 눌러 github 페이지로 온 다음, fork를 누른다.

![pic2](/assets/img/readme2.PNG)



3. 내 repository로 온 뒤 settings에서 repository name을 바꿔준다.

![pic3](/assets/img/readme3.PNG)





### title, logo 등 수정

`_config.yml` 파일을 수정해 title 과 logo 등을 수정한다.

```yaml
author_logo: piglet.png
author: Bomi Kwon
author_bio: Hi, my name is Bomi Kwon.
author_email: "kwonbomi@kookmin.ac.kr"
author_location: Korea
author_website_url: "https://github.com/bomi0320/"
typewrite-text: 안녕하세요 :D
hero_cover_img: JohnMayer.jpg # replace this for changing homepage cover (eg. try cover.jpeg). Image should be in /assets/img
```





### 카테고리 추가

`categories` 디렉토리 밑에 `java.md`, `python.md`, `markdown.md` 파일을 각각 만들어서 Blog에 java, python, markdown 카테고리를 추가한다.





### author 추가

1. `_authors` 디렉토리 아래에 `bomikwon.md` 파일을 만들고

2. `_data/authors.yml` 파일에 다음 코드를 추가해서 author를 추가한다.

```yaml
bomikwon:
   name: Bomi Kwon
   username: bomikwon
   site: https://bomikwon.com
   avatar: piglet.png
   bio: "Hi, I'm Bomi Kwon"
   email: kwonbomi@kookmin.ac.kr
   social:
      - title: "github"
        url: "https://github.com/bomi0320/bomi0320.github.io"
```





### 댓글 기능 추가

1. _config.yml 파일에 disqus short name을 추가하고

```yaml
disqus_shortname: bomiblog-1
```

2. _includes/blog_post_article.html 파일에서 아래처럼 수정해서 댓글 기능을 추가한다.

```html
  {%- if site.disqus_shortname -%}
  <div class="comments">
    {%- include blog_post_comments.html -%}
   </div>
    {%- endif -%}
       <div id="disqus_thread"></div>
```





### favicon 추가

1. favicon 이미지를 만든 후 asserts/img/logo/favicon.ico에 이미지를 저장한다.
2. _includes/head.html 파일을 수정해 favicon을 추가한다.

```html
<link
    rel="icon"
    href="{{site.url}}{{site.baseurl}}/assets/img/logo/favicon.ico"
    type="image/x-icon"
    sizes="16x16"
  />
```



