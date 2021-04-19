### 一、	项目中的icon图标：
升级后很多icon名称发生了变化导致无法显示，需要去文档查看最新的icon名称

### 二、	Button：
为了方便使用第三方图标，Button 的 icon 属性现在需要传入完整的图标类名

### 三、	Checkbox：
Checkbox的change事件中，参数由event变为了value

### 四、	Input：
1.移除了input的icon属性。现在通过suffix-icon或者suffix具名插槽来加入尾部图标
2.移除on-icon-click和click事件，现在如果需要为输入框中的图标添加点击事件，请以具名 slot 的方式添加图标
3.change 事件现在仅在输入框失去焦点或用户按下回车时触发，与原生 input 元素一致。如果需要实时响应用户的输入，可以使用 input 事件
4.盒模型从block修改为inline-block
5.Input的id属性被传递到了最底层的input元素，需要关注有id的el-input

### 五、	Select：
1.盒模型从block修改为inline-block
2.Select，值为对象类型时，需要提供一个 value-key 作为唯一性标识
3.Select，过滤情况下，placeholder 为选中选项的 label

### 六、	Switch：
1.由于 on-* 属性在 JSX 中会被识别为事件，导致 Switch 所有 on-* 属性在 JSX 中无法正常工作，所以 on-* 属性更名为 active-*，对应地，off-* 属性更名为 inactive-*。受到影响的属性有：on-icon-class、off-icon-class、on-text、off-text、on-color、off-color、on-value、off-value
2.active-text 和 inactive-text 属性不再有默认值

### 七、	TimePicker：
点击清空按钮时，change中的参数由’’变为null

### 八、	DatePicker：
同timepicker

### 九、	DateTimePicker：
同timepicker

### 十、	Upload：
Upload 重构升级，default-file-list 属性更名为 file-list, show-upload-list 属性更名为 show-file-list，thumbnail-mode 属性被移除


### 十一、	Form组件：
1.Form validateField() 方法回调的参数更新
2.Form移除输入框的成功状态

### 十二、	Table组件：
1.移除通过 inline-template 自定义列模板的功能
2.sort-method 现在和 Array.sort 保持一致的逻辑，要求返回一个数字
3.将 append slot 移至 tbody 元素以外，以保证其只被渲染一次
4.expand 事件更名为 expand-change，以保证 API 的命名一致性
5.row-class-name 和 row-style 的函数参数改为对象，以保证 API 的一致性

### 十三、	Tag：
type 属性现在支持 success、info、warning 和 danger 四个值

### 十四、	Pagination：
表单组件的 change 事件和 Pagination 的 current-change 事件现在仅响应用户交互

### 十五、	Loading：
非全屏 Loading 遮罩层的 z-index 修改为 2000；全屏 Loading 遮罩层的 z-index 值会随页面上的弹出组件动态更新

### 十六、	Tabs：
1.盒模型从 inline-block 修改为 block，Tab-Pane 移除 label-content 属性
2.Tabs 现在内部不再维护 tab 实例，需要在外部通过相关事件去处理

### 十七、	Dropdown：
1.menu-align 属性变更为 placement，增加更多方位属性
2.show-timeout 和 hide-timeout 属性现在仅在 trigger 为 hover 时生效

### 十八、	Dialog：
1.Dialog 的遮罩层现在默认插入至 body 元素上
2.移除 size 属性。现在 Dialog 的尺寸由 width 和 fullscreen 控制
3.移除通过 v-model 控制 Dialog 显示和隐藏的功能

### 十九、	Tooltip：
1.重构 Tooltip，不再生成额外的 HTML 标签，确保被 tooltip 包裹的组件的结构不变

2.el-tooltip标签中，子元素如果有v-if，则需要为el-tooltip也加上v-if
