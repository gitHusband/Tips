# Tips
Tips is a jQurey plug-in that facilitates the generation of prompt information which is in the middle or other location relative to any parent element.

# 使用方法
将 jquery-tips 文件夹包含到你的项目并引用。

    * 第一种方法，用于特殊需求定制
    $.tips({
        parentElement: "",          //基准方位元素
        position: "middle",         //tips 位置，左上角，上居中，右上角，左居中，全居中，右居中，左下角，下居中，右下角，自定义相对位置，浮动
        positionFix: true,          //计算tip定位时，true - 考虑tip 宽高，false - 不考虑； 默认true。
        float: {                    //浮动参数，当position = 'float'时，可选；其余情况不需要 
            type: 'default',            //若不使用floatPositionFun, 可选择默认浮动方法
            cusFloatOptions: null,      //自定义浮动选项
            cusFloatStatus: null,       //自定义浮动初始状态，top，left等
            cusFloatFun: null,          //自定义浮动方法
            cusFloatCallback: $.noop,   //自定义浮动回调函数
        },
        group: {                    //分组，多个Tips 集合
            name: null,                 //分组名称
            len: 9999,                  //一个分组最大Tips个数
        },
        type: "normal",             //tips 样式, 支持自定义样式（传入class名称）
        limit: true,                //限制Tips 的大小
        icon: true,                 //是否显示icon
        background: false,          //false - 不显示遮罩层覆盖父元素， true - 显示遮罩层覆盖父元素
        destroy: "auto",            //auto - 自动销毁tips，manual - 不自动销毁tips，需手动销毁, never - 从不销毁tips
        delay: 2000,                //自动销毁tips 延时，单位：ms
        html: false,                //false - 文本类型信息，true - dom元素类型信息
        msg: [],                    //传入数组可换行
        htmlCallback: $.noop,       //dom元素回调函数，用于监听dom元素动作
        callback: $.noop            //公共回调函数
    });

    * 第二种方法，用于简单调用
    $.tips().success(msg, parentElement);
