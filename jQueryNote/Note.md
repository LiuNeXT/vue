示例

jQuery笔记

您也许已经注意到在我们的实例中的所有 jQuery 函数位于一个 document ready 函数中：
$(document).ready(function() {});
-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -
这是为了防止文档在完全加载（ 就绪） 之前运行 jQuery 代码。

$(this).hide() - 隐藏当前元素

$("p").hide() - 隐藏所有段落

$(".test").hide() - 隐藏所有 class = "test"
的所有元素

$("#test").hide() - 隐藏所有 id = "test"
的元素



$(document).ready(function) 将函数绑定到文档的就绪事件（ 当文档完成加载时）
$(selector).click(function) 触发或将函数绑定到被选元素的点击事件
$(selector).dblclick(function) 触发或将函数绑定到被选元素的双击事件
$(selector).focus(function) 触发或将函数绑定到被选元素的获得焦点事件
$(selector).mouseover(function) 触发或将函数绑定到被选元素的鼠标悬停事件


Post传参
$("button").click(function() {
    $.post("demo_test_post.asp", {
            name: "Donald Duck",
            city: "Duckburg"
        },
        function(data, status) {
            alert("Data: " + data + "\nStatus: " + status);
        });
});