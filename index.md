<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的个人主页</title>
    <!-- 确保引入了Minima主题的样式 -->
    <link rel="stylesheet" href="{{ '/assets/css/minima.css' | relative_url }}">
</head>
<body>
    <header class="site-header" role="banner">
        <div class="wrapper">
            <a class="site-title" rel="author" href="{{ '/' | relative_url }}">我的个人主页</a>
            <nav class="site-nav">
                <!-- 可以在这里添加导航链接 -->
            </nav>
        </div>
    </header>

    <div class="page-content">
        <div class="wrapper">
            <h1>欢迎来到我的主页</h1>
            <p>这里是我分享知识和个人想法的地方。</p>
            
            <!-- 添加一个介绍性的段落 -->
            <p>我是[你的名字]，一个热爱编程和探索新技术的人。在这个网站上，我会分享一些编程教程、技术文章以及我个人的一些思考。</p>
            
            <!-- 添加一些特色部分 -->
            <section>
                <h2>最新文章</h2>
                <!-- 使用Jekyll标签遍历最近的文章 -->
                {% for post in site.posts limit:5 %}
                    <article class="post-excerpt">
                        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
                        <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
                    </article>
                {% endfor %}
            </section>
            
            <section>
                <h2>联系方式</h2>
                <ul>
                    <li><strong>Email:</strong> <a href="mailto:name@example.com">name@example.com</a></li>
                    <li><strong>Twitter:</strong> <a href="https://twitter.com/johndoe">@johndoe</a></li>
                    <!-- 可以继续添加其他的社交网络链接 -->
                </ul>
            </section>
        </div>
    </div>

    <footer class="site-footer h-card">
        <data class="u-url" href="{{ '/' | relative_url }}"></data>
        <div class="wrapper">
            <p class="text-center">&copy; {{ site.time | date: '%Y' }} - {{ site.title }}</p>
        </div>
    </footer>
</body>
</html>
