# SMDropDownList
手持设备中使用原生select下拉控件效果并不尽人意，SMDropDownList下拉弹框支持(多选/单选)，适用于移动端下拉效果，依赖Jquery，有问题请发邮件：sm0210@qq.com

## 效果

![](https://github.com/sm0210/SMDropDownList/blob/master/SMDropDownList.jpg "SMDropDownList")

## 实例化组件
````
//模拟数据
		var data = [
			{name:'下拉选项一',id:'00000010110302063'},
			{name:'下拉选项二',id:'00000010110302064'},
			{name:'下拉选项三',id:'00000010110302065'},
			{name:'下拉选项四',id:'00000010110302066'},
			{name:'下拉选项五',id:'00000010110302067'}
		];
//参数配置    
var config = {
      //可配置参数：标题
      title: '下拉选择框',
      //必须参数：结果集
      result: data,
      //必须参数：模板
      itemTpl: [
        '<div class="ui-list-info">',
        '<h4 class="ui-nowrap left">${id}<span class="ui-nowrap-span">${name}</span></h4>',
        '</div>',
      ],
      //是否显示标题
      //isShowTitle: false,
      //可配置参数：1.false,随内容撑出高度，2.num：固定高度，超出滚动显示,默认[220]
      //fixedHeight: false,
      //可配参数：选择完成后是否自动关闭,默认[true]
      //autoClose: false,
      //可配置参数：每行是否显示右边箭头，默认[false]
      //rightArrow: false,
      //可配置参数：是否多选[默认单选]
      checkbox: true,
      //单击item事件
      onClick: itemClick
        	};
		//实例化下拉组件
		var smDropDownList = $.initSMDropDownList(config);
}); 
 ````
 
 ## 显示下拉组件
 ````
  //1.参数配置中传入data数据，直接显示
  smDropDownList.show();
  //2.显示时传入data数据
  smDropDownList.show(data);
 ````
 
 ## 监听事件
````
  function itemClick(data){
  //
  console.log(data);
  }

 ````
 
 ###如果您觉得此文有帮助，可以打赏点钱给我支付宝sm0210@qq.com ，或扫描二维码
![](https://github.com/sm0210/SMCalendar/blob/master/sm0210%40qq.com.jpg "sm0210@qq.com")


