品牌管理案例：
	过滤器   :  Vue.js 允许你自定义过滤器，可被用于一些常见的文本格式化。过滤器可以用在两个地方：双花括号插值和 v-bind 表达式。
	自定义键盘修饰符
	自定义指令
	生命周期(比较深，可以跳过)
	实现数据请求(vue-resource)
	
lib:存放非vue的第三方组件




数组操作【数组下标0开始，forEach   some   filter   findIndex 都会对数组中的每一项，进行遍历】：

1. splic(i, 2) : 删除数组元素【从i位置删除2个元素】

          this.list.splice(index, 1);

2. some : 根据指定的条件进行判断，返回true自动终止循环方法。
        del(id) //删除方法
		{
          this.list.some((item, i) => {
            if (item.id == id) {
              this.list.splice(i, 1);
              return true;
            }
          });
        }
		
3. findIndex : 找出符合条件的元素下标
        del(id) //删除方法
		{
          var index = this.list.findIndex
		  (item => 
			  {
				if (item.id == id) 
				{
				  return true;
				}
			  }
		  );
          this.list.splice(index, 1);
        }
		
4. push : 向数组添加新元素
        list: 
		[
          { id: 1, name: '奔驰', ctime: new Date() },
          { id: 2, name: '宝马', ctime: new Date() }
        ]
        var car = { id: this.id, name: this.name, ctime: new Date() }
        this.list.push(car);
		
5. forEache : 循环遍历【不循环完一般不会终止】
		var newList = []
		this.list.forEach(item => {
		  if (item.name.indexOf(keywords) != -1) {
			newList.push(item);
		  }
		});
		return newList;
		
6. filter : 遍历数组【一般用来过滤，返回值是符合条件的数组】
		return this.list.filter(item => {
            if (item.name.includes(keywords)) {
              return item;
            }
        });
		
		
		
ES6中字符串操作方法:
1.判断是否包含某段字符串
	String.prototype.includes('要包含的字符串'); -----> 如果包含，则返回 true ，否则返回 false。
	item.name.includes(keywords);
	
2.字符串在另一个字符串首次出现位置【可以用来判断是否包含】。
    item.name.indexOf(keywords) != -1 ;   ------> indexOf返回某个指定的字符在某个字符串中首次出现的位置。如果没有找到就返回-1。
	
	
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		
		



