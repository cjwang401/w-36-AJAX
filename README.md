# w-36-AJAX
let response = new XMLHttpRequest()
response.open('请求的动作', '请求的网址')
response.send()
response.onreadystatechange = () => {
    if (response.readyState === 4){
        if (response.status >= 200 && response.status < 300){
            let string = response.responseText
            let object = window.JSON.parse(string)
        }
    }
}
