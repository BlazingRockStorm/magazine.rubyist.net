---
layout: post
title: Rubyでプログラミングを教えた経験談
short_title: My Experience on Teaching Programming with Ruby
tags: 0064
post_author: ホアンクアン
created_on: 2024 年 6 月 11 日
---

{% include base.html %}

# 日本語バージョン：

## はじめに

IT業界全般、特にプログラミングは、人材育成は大事なことです。ですが、新しいメンバーをトレーニングするとき、メンターとしてエンジニアは、様々なチャレンジに会います。この投稿は、私の経験や、なぜRubyを選んでプログラミングを教えているかの理由です。よろしくお願いします。

## 自己紹介

初めまして。

ベトナムのハノイ出身のホアン・クアンです。４年間日本で働いています。今はリードエンジニアとして東京のITスタートアップで働いています。Agile/Scrum、AWSとRubyが好きです。

社会人になって最初の１年半、Rubyプログラマーでした。その後、システムエンジニアとして仕事しています。仕事ではあまりRubyを使っていませんが、自分でRubyを勉強し続けています。

よろしくお願いします。

## 状況

会社設立当初、CEOが知り合いをインターンやバイトとして雇いたいということで、リードエンジニアである私は彼らの育成も任されました。CEOの知り合いは、6人の若いベトナム人留学生でした。彼らは、卒業後、IT関連の仕事に就きたいと望んでいました。そのため私は自分のスキルと経験を彼らに伝えたいと思いました。しかし、...

### チャレンジ#1

私のケースは、これらの問題に合いました：
1. 留学生たちは日本語学校やIT専門学校で勉強していましたが、その学校でITやプログラミングをあまり勉強していませんでした。
1. IT関連の仕事をやりたいですが、彼らは具体的に何をするが分からなかったです。
1. 最近、私のベトナムコミュニティーに、「プログラミングできず、IT仕事もできる」というコースもあります。というのは、ベトナムのアウトソース会社は、3ヶ月から6ヵ月ぐらい、ITを知らない人にBrSE（ブリッジSE）になるためことを教えることです。そのことは、だいたいビジネスアナリスト(BA)の知識ですから、プログラミングは全然ないです。すなわち、留学生たちとして、「簡単より道」です。
1. 英語が分からなくて、日本語能力もまだ強くなかったです。
1. 問題があったら、資料や本を読まずに、ネットで検索せずに、すぐに聞きます。
1. 育成期間は3ヶ月だけでした。
1. プログラミング言語が多いです。
1. シラバスがまだなかったです。

上記のことから、解決ために、適切なプログラミング言語を選択し、それを使用して週ごとにシラバスを作成し、他のソリューションと組み合わせる必要がありました。

### チャレンジ#1の解決
私の対策方法は:
- 1、6、7の問題は、シンタックスが理解しやすく、早く勉強できるプログラミング言語を選びました。
- 2の問題は、彼たちへオリエンテーションを企画しました。
- 3の問題は、選んだプログラミング言語とオリエンテーションでした。プログラミング言語ソリューションに関しては、他の短期コースと競合するのに十分な速さで学習できる言語を選択する必要がありました。
- 4、5の問題は、彼たちに[「Read - Search - Ask」](https://www.freecodecamp.org/news/read-search-dont-be-afraid-to-ask-743a23c411b4/)を教え、参考資料をちゃんと準備しました。
- 8の問題は、週ごとにシラバスを作成するしかありませんでした。

この投稿に限り、**「シンタックスが理解しやすく、早く勉強できるプログラミング言語を選ぶ」**方法をもっと続けたいです。Ruby、PythonやTypescriptは、学習が簡単ですぐに習得できるというこの要件を満たしています。

このとき、Pythonを選びました。理由は：
- Rubyのシンタックスに似ています。
- AWSに働くとき、Lambda、Glue ETLのようなサービスに、Pythonを使うことがたくさんです。ですから、私も経験もあります。
- CEOの意見でしたから🙁

### チャレンジ#2：なぜPythonからRubyに変わりましたか？

プログラミング言語を選らびましたが、新しい問題が発生しました：
- 留学生たちのコードは、Pythonのインデントに関するバグが多かったです。
- オブジェクト指向(OOP)に、Pythonのアクセス修飾子はわかりにくかったです。

Pythonのアクセス修飾子
```python
class Example:
  # public場合は、_がないです
  def public_method:
    pass
  
  # protected場合は、_が1つあります
  def _protected_method:
    pass
   
  # protected場合は、__が2つあります
  def __private_method:
    pass
```
留学生たちに「このアンダースコアの意味はなんですか」を聞いたら、全然分からなかったです。

このとき、本当のOOP言語を選びました。OOPといえば、多分Javaですが、すぐに習得できないです。彼たちは日本語学校や専門学校の学生で、ITを勉強している大学３年生ではなかったです。ですから、Rubyを選びました。

Rubyのアクセス修飾子
```ruby
class Example
  # public場合は、指定されていないかpublicキーワードです。
  def public_method
  end

  # protected場合は、protectedキーワードです。
  protected

  def protected_method
  end

  # private場合は、privateキーワードです。
  private

  def private_method
  end
end
```
### 結果

PythonからRubyに変えたあと、留学生たちは：
- 1日後、すぐにRubyのコードを書けました。
- コードの書き方が厳格になり、より慎重になっていました。
- 学生たちはOOPの基本概念をよく理解していました。
- 論理的思考が向上しました。なぜならOOPはプログラミングをする時の考え方によい方向性をしています。

その後、Rubyのコアを分かったら、Ruby on Railsを勉強して、興味のあるプロジェクトを作りました。でも、結局、3人はプログラミングなしでIT仕事をしたかったため、大きなベトナムアウトソース会社に入りました。1人は、日本語学校に戻って勉強を続けました。2人だけプログラミング続けています。

ちょっと寂しかったです。

## おわりに

私にとって、Rubyは教育するのにいいプログラミング言語です。Rubyプログラマーコミュニティをもっとサポートできたらいいのにと思います。

最後までお読みいただき、ありがとうございます。

------

# English version:

## Intro

In the IT industry in general and programming particularly, training new members is very important. However, when training them, there are a lot of challenges that the mentor engineer has to solve. The article is my experience and the reason why I choose Ruby as the way to teach programming and the results.

## Self Introduction

Hello, my name is Hoang Quan. I'm from Hanoi, Vietnam. I'm working in Japan for 4 years. At the moment, I'm the Lead Engineer of a start up in Tokyo. My favorite tech stack is Agile/Scrum, AWS and Ruby.

At the first 1,5 years of my career, I worked as a Ruby developer. Then, after becoming a system engineer, although I rarely use Ruby in work, I continue to learn Ruby myself.

## Situation

At the beginning of the company, the CEO want to hire some of his acquaintances as the company interns and part-time, so as the lead engineer, I am also tasked with training them. They were 6 young Vietnamese overseas students with a lot of energy and eager to find IT related jobs. I was really excited and hoped that I can teach them all my skills and experiences. But then...

### Challenges

In my case, these are my problems:

- They are the students of the IT vocational schools and the Japanese-language schools, so they didn't learn much about IT and programming from those schools.
- They don't know in particular who they will become when "having an IT job".
- Recently, our Vietnamese has the "You can have an IT job without programming". The outsourcing companies have the programs that produce a BrSE for 3-6 months. Those programs are just BA courses, so no programming. With the students of the IT vocational schools and the Japanese-language schools, these are "the easy way".
- Their English and Japanese are not so good.
- My time for the training is only 3 months.
- There are many programming languages as the options.
- There is no syllabus at that time.

With the above, I have to choose the appropriate programming language, build a syllabus with it weeks by weeks, combine with other solutions. 

### Solution to Challenge #1

My solutions are:
- For issues 1, 6, and 7, choose a programming language that is easy to understand the syntax and can be learned quickly.
- For issue 2, I organized an orientation for them.
- For issue 3, it's the programming language I chose and the orientation. For the programming language solution, I need to choose a language that can be learned fast enough to compete with other short courses.
- For issues 4 and 5, I teach them to ["Read - Search - Ask"](https://www.freecodecamp.org/news/read-search-dont-be-afraid-to-ask-743a23c411b4/) and prepare reference materials properly.
- For issue 8, I have no choice but to create a syllabus for each week.

Within the limits of the article, I would like to continue with the solution of **"Choose a programming language that is easy to understand the syntax and can be learned quickly"**. Ruby, Python, and Typescript meet this requirement of being easy to learn and quick to master.

At that time, I chose Python. Reasons are:
- Similar to Ruby syntax.
- When I work with AWS, I use Python a lot for services like Lambda and Glue ETL. So I am also familiar with Python.
- Because it was the CEO's opinion 🙁

### Challenge #2: Why did I change from Python to Ruby?

After choosing a programming language, new problems arose:
- The students' code had many bugs related to Python indentation.
- In object-oriented (OOP), Python's access modifiers are difficult to understand.

Python access modifiers
```python
class Example:
# If public, there is no _
def public_method:
pass

# If protected, there is one _
def _protected_method:
pass

# If protected, there are two __
def __private_method:
pass
```
When I asked the students, "What does this underscore mean?", they had no idea.

At this point, I chose a real OOP language. Speaking of OOP, it's probably Java, but it's difficult to learn it right away. They were students at Japanese language schools and vocational schools, not third-year university students studying IT. That's why they chose Ruby.

Access modifiers in Ruby
```ruby
class Example
# For public, it's free or public keyword.
def public_method
end

# For protected, it's protected keyword.
protected

def protected_method
end

# For private, it's private keyword.
private

def private_method
end
end
```
### Results

After switching from Python to Ruby, the students:
- After one day, they were able to write Ruby code immediately.
- Writing code became more rigorous, so they were more careful.
- They understood the four basic concepts of OOP well.
- Their logical thinking improved, because OOP is a good direction for thinking when programming.

After that, after understanding the core of Ruby, they studied Ruby on Rails and created interesting projects. But in the end, three of them wanted to get an IT job without programming, so they joined a large Vietnamese outsourcing company. One went back to Japanese language school and continued studying. Only two continued programming.

It was a little sad.

## Conclusion

For me, Ruby is a good programming language for education. I wish I could support the Ruby programmer community more.

Thank you for reading to the end.