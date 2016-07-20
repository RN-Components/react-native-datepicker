# react-native-datepicker
react-native datePicker component both of iOS and Android


## usage
```js
const DateText = (<View><Text style={styles.buttonText}>{moment(this.state.date).format('YYYY') }</Text><Text style={[styles.buttonText, styles.buttonMonText]}>{moment(this.state.date).format('MM') }月</Text></View>)

<DatePicker
  style={{width: 250}}
  date={this.state.date}
  mode="date"
  format="YYYY-MM-DD"
  actionComponent={DateText}
  minDate=""
  maxDate=""
  confirmBtnText="确定"
  cancelBtnText="取消"
  customStyles={{
   
  }}
  onDateChange={(date) => {this.setState({date: date})}}
/>
```
## Properties

- style	-	object	定义日期的样式，比如宽高
- date	-	string 设置日历显示的日期
- mode	'date'	string 选择时间格式，有 'date', 'time','datetime' 三种
- format	'YYYY-MM-DD'	string	时间格式化
- confirmBtnText	'确定'	string	选择日期按钮的文字，默认是 「确定」
- cancelBtnText	'取消'	string 取消日期按钮的文字，默认是 「取消」
- iconSource	-	{uri: string} | number  日历的 icon ，如果需要的话
- minDate	-	string | date	最小可选的日期
- maxDate	-	string | date	最大可选择的日期
- duration	300	number	弹窗显示日历组件的动画，默认300ms
- customStyles	-	number	自定义日历的样死
- showIcon	true	boolean	是否需要显示日历的icon
- actionComponent - 触发日历控件的组件，可以是输入框也可以是文字或者其他的组件，样式内容都可以自定义

## method

onDateChange 选择日期