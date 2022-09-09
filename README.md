## answer-search-bank

### 描述 description

整合网上题库到`answer-search API`

### 关于 `answer-search API`

基础 URL: `https://api.answer.uu988.xyz:4545`

1. 题目搜索

   - 路径: `/answer/search`

   - 请求方式: `POST`

   - 请求类型: `application/json`

   - 请求体:

     ```javascript
     {
       question: '题目内容';
     }
     ```

   - 响应体:

     ```javascript
     {
       errno: 0,
       message: "消息",
       data: {
        question: "题目内容",
        answers: [
          "答案1",
          "答案2",
        ],
        from: "来源题库"
       }
     }
     ```

   - 示例:

     - 请求体

       ```javascript
       {
         question: '新时期要注重选拔任用（）、（）、（）、（）、（）的干部，对政治不合格的干部实行“一票否决”，已经在领导岗位的坚决调整。';
       }
       ```

     - 响应体

       ```javascript
        {
          errno: 0,
          message: "search success",
          data: {
           question: "新时期要注重选拔任用（）、（）、（）、（）、（）的干部，对政治不合格的干部实行“一票否决”，已经在领导岗位的坚决调整。",
           answers: [
              "A",
              "B",
              "C",
              "D",
              "E"
           ],
           from: "https://www.yisouti.com/search"
          }
        }
       ```

2. 题库查询

   - 路径: `/answer/bank`

   - 请求方式: `POST`

   - 响应体:

     ```javascript
     {
       errno: 0,
       message: "消息",
       data: {
        bank: [
          "题库1",
          "题库2",
        ],
       }
     }
     ```

   - 示例:

     - 响应体

       ```javascript
        {
          errno: 0,
          message: "get bankList success",
          data: {
           bank: [
           "https://a6.qikekeji.com/txt/data/detail",
           "http://www.syiban.com/search/index/init.html",
           ]
          }
        }
       ```

### 已知题库

- [https://a6.qikekeji.com](https://a6.qikekeji.com/txt/data/detail)
- [http://www.syiban.com](http://www.syiban.com/search/index/init.html)
- [https://www.hysgn.com](https://www.hysgn.com/e/search/index.php)
- [https://www.yisouti.com](https://www.yisouti.com/search)
- [https://www.zhaokaoti.com](https://www.zhaokaoti.com/Search/Index)

### 提交新题库

- 要求

  1. 无登录注册需求

  2. 无查询次数限制

  3. 题库访问不卡顿，响应迅速，题量尽量大，错误率低

  4. 答案简洁，不出现图片、视频、音频等不直接的答案

  5. 题型包含选择、填空、判断等

- 途径

  1. `GitHub`

     在 [Issue](https://github.com/Xu22Web/answer-search-bank/issues) 中反馈新题库信息

  2. `email`

     发送新题库到 [QQ 邮箱](mailto:1627295329@qq.com) `1627295329@qq.com`
