    /**
     * 获取地址栏URL参数
     * @param name
     * @returns result | null
     */
    function getUrlParam(name) {
        var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)");  //构造正则表达式对象
        var r = decodeURI(window.location.search).substr(1).match(reg);  //匹配目标参数
        return r === null ? r : r[2];
    }