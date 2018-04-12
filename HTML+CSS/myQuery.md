```js
/**
 * 对DOM的查找进行了封装，可以根据ID、类名或标签名进行查询
 * @param val               查询的内容
 * @returns {*}
 */
function $(val) {
    if (val.charAt(0) === '#') {
        return document.getElementById(val.substr(1));
    } else if (val.charAt(0) === '.') {
        return document.getElementsByClassName(val.substr(1));
    } else {
        return document.getElementsByTagName(val);
    }
}

/**
 * 兼容IE8及以前版本使用getElementsByClassName
 * @param val               需要查找的类选择器名称
 * @returns {Array}
 */

function getByClassName(val) {
    // 如果类选择器以.开始，需要把.去掉
    var className = val.indexOf('.') == 0 ? val.slice(1) : val;
    var arr = [];
    var all = $('*');

    for (i = 0, len = all.length; i < len; i++) {
        var tmp = all[i].split(' ');

        for (var j = 0, count = tmp.length; j < count; j++) {
            if (tmp[j] == className) {
                arr.push(all[i]);
                break;
            }
        }
    }
}


/**
 * 获取scrollTop和scrollLeft
 * @returns {{top: number, left: number}}
 */
function scroll() {
    if (document.compatMode === 'BackCompat') {  // 使用使用DTD的情形
        return {
            top: document.body.scrollTop,
            left: document.body.scrollLeft
        };
    } else if (window.pageYOffset) {
        return {
            top: window.pageYOffset,
            left: window.pageXOffset
        }
    } else if (document.documentElement.scrollTop) {
        return {
            top: document.documentElement.scrollTop,
            left: document.documentElement.scrollLeft
        };
    }
    return {top: 0, left: 0};
}

// 如果浏览器不支持getElementsByClassName，重写getElementsByClassName的实现行为
document.getElementsByClassName = document.getElementsByClassName ? document.getElementsByClassName : getByClassName;

/**
 * 对传递进行的盒子模型对象进行X轴的移动
 * 
 * @param obj 形参，表示这个函数需要操作的标签
 * @param target 操作标签需要移动的X坐标
 */ function animationX(obj ,target) {

    obj.timer = setInterval(function () {
        var speed = (target - obj.offsetLeft) / 10;

        speed = speed > 0 ? Math.ceil(speed) : Math.floor(speed);

        obj.style.left = obj.offsetLeft + speed + 'px';

        if (obj.offsetLeft == target){
            clearInterval(obj.timer)
        } 
    },10);
}

/**
 * 对传递进行的盒子模型对象进行Y轴的移动
 * 
 * @param obj 形参，表示这个函数需要操作的标签
 * @param target 操作标签需要移动的Y坐标
 */ function animationY(obj ,target) {

    obj.timer = setInterval(function () {
        var speed = (target - obj.offsetTop) / 10;

        speed = speed > 0 ? Math.ceil(speed) : Math.floor(speed);

        obj.style.top = obj.offsetTop + speed + 'px';

        if (obj.offsetTop == target){
            clearInterval(obj.timer)
        } 
    },10);
}

```