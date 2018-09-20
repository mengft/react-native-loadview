# react-native-loadview
基于React Native实现的界面加载组件，

## Installation

```bash
npm install react-native-loadview --save
```

## Import into your project

```js
import LoadView from 'react-native-loadview';
```

## Examle useage
用于界面数据处理load状态展示，目前支持两种gif加载方式

```js
<LoadView style={Styles.loadView} visible={this.props.showIndicator} gif='triangles' />
```
```js
<WebView
    source={{ uri: url }}
    onShouldStartLoadWithRequest={e => this.onShouldStartLoadWithRequest(e)}
    startInLoadingState
    onError={e => this.onError(e)}
    renderLoading={() => <LoadView/>}
    renderError={() => this.renderError()}
    onNavigationStateChange={e => this.onNavigationStateChange(e)}
/>
```

## Properties
属性  | 描述    | 类型  | 默认    
------ | ------ | ------  | ------
iconSize  | gif大小 | ``` PropTypes.number ``` | 40
message | 加载文本  | ``` PropTypes.string ``` |   
visible | 是否显示  | ``` PropTypes.bool ```  | true 
gif | gif名称  | ``` PropTypes.oneOf(["spinner", "triangles"]) ```  | 'spinner'
