# dom-lazyLoad<br>

页面的内容只有滚动到屏幕区域内才加载,提升性能<br>
原理就是把需要滚动加载的dom内容放进一个textarea里，然后用一个容器包裹住,当这部分内容高度出现在屏幕中的时候，就释放出textarea中的值append到容器中，实现滚动加载<br>
creatEle: function (targetElm, callback)，如果加载的内容没有绑定js相关功能，则可以省略第二个callback函数，否则的话需要传入callback函数名，比如轮播插件等等：GLOBAL.lazyLoad.creatEle("textarea.js_buyShowslide", initBuyerShowImg)<br>
