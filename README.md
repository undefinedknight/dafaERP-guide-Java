# 前言

这篇大发项目JAVA开发指导，是我从接手之前的项目继续开发到现在，遇到的一些经验的总结，并不一定全都正确，但是实现功能上大概没有问题。

另外这篇指导几乎都是使用“应收款状态日期录入”模块的代码，因为这部分是我接手以来从最初开始开发的，而不是基于已有代码的修改。

编写这篇GITBOOK主要是为了方便之后的Java开发人员，有案例可循，算是一个开发参考手册吧。 

use advancedEmoji to print a smile: 😄 😭

<video src="../videos/言叶之庭 OST.mp4" width="100%" controls="controls" poster="../videos/言叶之庭Cover.jpg"></video>


{%ace edit=false, lang='javascript',theme="monokai"%}
function querySearchData(field, from, to, xmwbs){
    var conditions = new Array()
    if(field){
        var condition = createOneCondition("FIELD", field, "EQ")
        conditions.push(condition)
    }
    if(from){
        var condition = createOneCondition("FROM", from, "EQ")
        conditions.push(condition)
    }
    if(to){
        var condition = createOneCondition("TO", to, "EQ")
        conditions.push(condition)
    }
    if(xmwbs){
        var condition = createOneCondition("XMWBS", xmwbs, "EQ")
        conditions.push(condition)
    }
    var condition = createCondition(conditions)
    var param = {
        item: JSON.stringify(condition)
    }

    // 封装好的请求方式，该请求方式会添加loading状态显示
    callAjax($("#basePath").val() + "receivables-report/fetchSearchData", "POST", param, function(res){
    //some code…      
    })
}
{%endace%}

{% exercise %}
Define a variable `x` equal to 10.
{% initial %}
var x =
{% solution %}
var x = 10;
{% validation %}
assert(x == 10);
{% context %}
// This is context code available everywhere
// The user will be able to call magicFunc in his code
function magicFunc() {
    return 3;
}
{% endexercise %}

