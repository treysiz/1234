<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>餐馆名 - 美味佳肴</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <header>
      <nav>
        <ul>
          <li><a href="#">首页</a></li>
          <li><a href="#">菜单</a></li>
          <li><a href="#">预订</a></li>
          <li><a href="#">联系我们</a></li>
        </ul>
      </nav>
    </header>
    
    <main>
      <section id="hero">
        <h1>欢迎来到餐馆名</h1>
        <h2>最棒的食物和氛围</h2>
        <a href="#" class="btn">预订</a>
      </section>
      
      <section id="about">
        <h2>关于我们</h2>
        <p>我们是一家专注于提供美味佳肴和舒适氛围的餐厅。我们使用最优质的食材和配料来制作我们的菜肴，并提供最好的服务给我们的客人。</p>
        <a href="#" class="btn">查看菜单</a>
      </section>
      
      <section id="menu">
        <h2>我们的菜单</h2>
        <p>我们提供各种各样的菜肴和饮品，从开胃菜到主菜，以及精选的红酒和鸡尾酒。</p>
        <a href="#" class="btn">查看菜单</a>
      </section>
      
      <section id="reservation">
        <h2>预订</h2>
        <p>请填写以下表格进行预订。我们会尽快与您联系以确认您的预订。</p>
        <form>
          <label for="name">姓名：</label>
          <input type="text" id="name" name="name" required>
          <label for="email">电子邮件：</label>
          <input type="email" id="email" name="email" required>
          <label for="date">日期：</label>
          <input type="date" id="date" name="date" required>
          <label for="time">时间：</label>
          <input type="time" id="time" name="time" required>
          <label for="guests">客人数量：</label>
          <input type="number" id="guests" name="guests" required>
          <button type="submit" class="btn">提交预订</button>
        </form>
      </section>
    </main>
    
    <footer>
      <p>版权所有 © 2023 餐馆名</p>
    </footer>
  </body>
</html>
