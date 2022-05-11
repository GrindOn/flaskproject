小结：
学习的标签
    <h1></h1>
    <h1></h1>
    <h1></h1>
    <h1></h1>
    <h1></h1>

·划分：
-块级标签：
    <h1></h1>
    <div></div>
-行内标签
    <span></span>
    <a></a>
    <img />

嵌套：
<div>
    <span>xxx</span>
    <img />
    <a></a>
</div>
2.4.5 超链接
跳转到其他网站
<a href="https://blog.csdn.net/geerniya/article/details/79233637">点击跳转</a>

跳转到自己网站的其他的地址

<a href="http://127.0.0.1:8000/show/other">点击跳转</a>
<a href="/show/other">查看更多</a>

# 当前页面打开
<a href="/show/other">查看更多</a>

# 新的tab页面打开
<a href="/show/other" target="_blank">查看更多</a>

2.4.6 图片

<img src="图片地址">

直接显示别人的图片地址（防盗链）：
<img src="https://image.baidu.com/search/detail?ct=503316480&z=0&ipn=false&word=iu&step_word=&hs=0&pn=3&spn=0&di=7077213605308923905&pi=0&rn=1&tn=baiduimagedetail&is=0%2C0&istype=0&ie=utf-8&oe=utf-8&in=&cl=2&lm=-1&st=undefined&cs=3117713125%2C581518945&os=1554597926%2C3860373156&simid=3117713125%2C581518945&adpicid=0&lpn=0&ln=1507&fr=&fmq=1652179069790_R&fm=&ic=undefined&s=undefined&hd=undefined&latest=undefined&copyright=undefined&se=&sme=&tab=0&width=undefined&height=undefined&face=undefined&ist=&jit=&cg=star&bdtype=0&oriquery=&objurl=https%3A%2F%2Fgimg2.baidu.com%2Fimage_search%2Fsrc%3Dhttp%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F202004%2F23%2F20200423224118_QZRj8.thumb.1000_0.jpeg%26refer%3Dhttp%3A%2F%2Fc-ssl.duitang.com%26app%3D2002%26size%3Df9999%2C10000%26q%3Da80%26n%3D0%26g%3D0n%26fmt%3Dauto%3Fsec%3D1654771073%26t%3Dedfe0769b55d27dafd1048f348fb1ec7&fromurl=ippr_z2C%24qAzdH3FAzdH3Fooo_z%26e3B17tpwg2_z%26e3Bv54AzdH3Fks52AzdH3F%3Ft1%3D8nndadlabc&gsm=4&rpstart=0&rpnum=0&islist=&querylist=&nojc=undefined&dyTabStr=MCwzLDYsNCw1LDcsOCwxLDIsOQ%3D%3D">

<img src="自己图片的地址">
显示自己的图片:
    -自己的项目中创建:static目录，图片要放在static
    -在页面上引入图片
    <img src="/static/iu.jpg" />

关于设置图片的高度和宽度
<img src="图片地址" stytle="height:100x; width:200px;" />
<img src="图片地址" stytle="height:10%; width:20%;" />

2.4.7
列表标签:
无序列表
<ul>
    <li>中国联通</li>
    <li>中国移动</li>
    <li>中国电信</li>
</ul>
有序列表
<ol>
    <li>中国联通</li>
    <li>中国移动</li>
    <li>中国电信</li>
</ol>

2.4.8 表格
<table border="1">
    <thead>
        <tr> <td>ID</td> <td>姓名</td> <td>年龄</td> </tr>
    </thead>
    <tbody>
        <tr> <td>10</td> <td>wqq</td> <td>19</td> </tr>
        <tr> <td>11</td> <td>wdc</td> <td>19</td> </tr>
        <tr> <td>12</td> <td>feb</td> <td>19</td> </tr>
        <tr> <td>13</td> <td>miki</td> <td>19</td> </tr>
        <tr> <td>14</td> <td>zxc</td> <td>19</td> </tr>
    </tbody>
</table>


2.4.9 input系列
# 文本框
<input type="text">
# 密码框
<input type="password">
# 文件选择框
<input type="file">
# 单选框
<input type="radio" name="n1"> 男
<input type="radio" name="n1"> 女
# 复选框
<input type="checkbox"> 篮球
<input type="checkbox"> 足球
<input type="checkbox"> 乒乓球
<input type="checkbox"> 棒球
# 按钮
<input type="button" value="提交"> -->普通的按钮
<input type="submit" value="提交"> -->提交表单

2.4.10 下拉框

<select>
    <option>北京</option>
    <option>上海</option>
    <option>广东</option>
</select>


2.4.11 多行文本
<textarea></textarea>

案例：用户注册



3.网络请求
·在浏览器的URL中写入地址，点击回车，访问。
    浏览器会发送数据过去，本质上发送的是字符串：
    "GET /explore http1......"

    "POST /explore http1......"
·浏览器想后端发送请求时：
    ·GET请求【URL方法、表单提交】
        ·现象：GET请求、跳转、向后台传入数据数据会拼接在URL上。
        https://www.baidu.com/s?ie=utf-8&f=8&rsv_bp=1&rsv_idx=1&tn=88093251_101_hao_pg&wd=iu&fenlei=256&oq=pycharm%25E8%25BF%2590%25E8%25A1%258C%25E8%25BF%259C%25E7%25A8%258B%25E6%259C%258D%25E5%258A%25A1%25E5%2599%25A8%25E4%25B8%258A%25E7%259A%2584%25E4%25BB%25A3%25E7%25A0%2581&rsv_pq=809fdafe0001ac79&rsv_t=7f47HDprTQ%2BtMYPeiZatu3WdRA9IM42moryExehl2Eka4xcxDddxNan702%2FuDz%2FENhu2cG3C%2F4uUhQ&rqlang=cn&rsv_enter=0&rsv_dl=tb&rsv_btype=t&inputT=1222&rsv_sug3=48&rsv_sug1=45&rsv_sug7=100&rsv_sug2=0&rsv_sug4=1222
        注意：GET请求数据会在URL中体现。
    ·POST请求【表单提交】
        ·现象：提交数据不在URL中而是在请求体中。