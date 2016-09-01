# ng-translude
ng-translude
ng-translude用在指令模版标签的属性中，代表指令中插入的标签是否嵌入，加了就表示嵌入，不加则不嵌入；
比如一个自定义指令'<tabs><tabs>',他的模板是'<div></div><div ng-translude></div>'，在引用的时候'tabs><input /></tabs>'，那么如果没加ng-translude的话，<input />这个标签是不能嵌入的会在删除，f12控制台也看不到，加了ng-transclude的话,<input>标签就会嵌入在加了ng-translude那个标签上;
比如代码'tabs><input /></tabs>'，控制台查看元素是'<div></div><div ng-translude><input /></div>',如果没加控制台审查结果会是'<div></div><div></div>'，<input>没有被嵌入。
