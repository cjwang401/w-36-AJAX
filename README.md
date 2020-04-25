# w-36-AJAX
// 1.使用XMLHttpRequest发送请求
let response = new XMLHttpRequest()
response.open('请求的动作', '请求的网址')
response.send()
// 2.服务器返回XML格式的字符串，现在XML已经淘汰，使用的是JSON
response.onreadystatechange = () => {
    if (response.readyState === 4){
        if (response.status >= 200 && response.status < 300){
            // 3.js解析XML，并更新局部页面
            let string = response.responseText
            let object = window.JSON.parse(string)
        }
    }
}
