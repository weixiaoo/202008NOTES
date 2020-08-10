##### 简易计算器

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script src="../lib/vue.min.js"></script>
	</head>
	<body>
		<div id="app">
			<input type="text" v-model="n1" />

			<select v-model="opt">
				<option value="+">+</option>
				<option value="-">-</option>
				<option value="*">*</option>
				<option value="/">/</option>
			</select>
			<input type="text" v-model="n2" />

			<input type="button" value="=" @click="calc" />

			<input type="text" v-model="result" />
		</div>
	</body>
</html>
<script>
	//创建vue实例 得到ViewModel
	var vm = new Vue({
		el: '#app',
		data: {
			n1: 0,
			n2: 0,
			result: 0,
			opt: '+',
		},
		methods: {
			calc() { //计算器算法的方法
			//第一种方法
				/* switch (this.opt) {
					//逻辑
					case '+':
						this.result = parseFloat(this.n1) + parseFloat(this.n2);
						break;
					case '-':
						this.result = parseFloat(this.n1) - parseFloat(this.n2);
						break;
					case '*':
						this.result = parseFloat(this.n1) * parseFloat(this.n2);
						break;
					case '/':
						this.result = parseFloat(this.n1) / parseFloat(this.n2);
						break;
				} */
			
			//第二种方法
			//注意：这是投机取巧的方式，正式开发中 ， 尽量少用
			var codeStr = parseFloat(this.n1) + this.opt +parseFloat(this.n2);
			this.result = eval(codeStr);
			}
		}
	});
</script>
```
