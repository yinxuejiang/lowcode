# 低码引擎代码

## 项目schema

```json
{
  "version": "1.0.0",
  "componentsMap": [
    {
      "package": "@alilc/antd-lowcode-materials",
      "version": "1.1.1",
      "exportName": "Icon",
      "main": "",
      "destructuring": true,
      "componentName": "Icon"
    },
    {
      "package": "@alilc/antd-lowcode-materials",
      "version": "1.1.1",
      "exportName": "Button",
      "main": "",
      "destructuring": true,
      "componentName": "Button"
    },
    {
      "devMode": "lowCode",
      "componentName": "Page"
    }
  ],
  "componentsTree": [
    {
      "componentName": "Page",
      "id": "node_dockcviv8fo1",
      "props": {
        "ref": "outerView",
        "style": {
          "height": "100%"
        }
      },
      "fileName": "/dashboard",
      "dataSource": {
        "list": [
          {
            "type": "fetch",
            "isInit": false,
            "options": {
              "params": {},
              "method": "GET",
              "isCors": true,
              "timeout": 5000,
              "headers": {},
              "uri": "mock/info.json"
            },
            "id": "info"
          }
        ]
      },
      "state": {
        "text": {
          "type": "JSExpression",
          "value": "\"outer\""
        },
        "isShowDialog": {
          "type": "JSExpression",
          "value": "false"
        }
      },
      "css": "body {\n  font-size: 12px;\n}\n\n.button {\n  width: 100px;\n  color: #ff00ff\n}",
      "lifeCycles": {
        "componentDidMount": {
          "type": "JSFunction",
          "value": "function componentDidMount() {\n  console.log('did mount');\n}",
          "source": "function componentDidMount() {\n  console.log('did mount');\n}"
        },
        "componentWillUnmount": {
          "type": "JSFunction",
          "value": "function componentWillUnmount() {\n  console.log('will unmount');\n}",
          "source": "function componentWillUnmount() {\n  console.log('will unmount');\n}"
        }
      },
      "methods": {
        "testFunc": {
          "type": "JSFunction",
          "value": "function testFunc() {\n  console.log('test func');\n}",
          "source": "function testFunc() {\n  console.log('test func');\n}"
        },
        "onClick": {
          "type": "JSFunction",
          "value": "function onClick() {\n  this.dataSourceMap['info'].load({\n    id: 1\n  });\n}",
          "source": "function onClick() {\n  this.dataSourceMap['info'].load({\n    id: 1\n  });\n}"
        },
        "onClick_new": {
          "type": "JSFunction",
          "value": "function onClick_new() {\n  this.dataSourceMap['infoList'].load({\n    id: 1\n  });\n}",
          "source": "function onClick_new() {\n  this.dataSourceMap['infoList'].load({\n    id: 1\n  });\n}"
        }
      },
      "originCode": "class LowcodeComponent extends Component {\n  state = {\n    \"text\": \"outer\",\n    \"isShowDialog\": false\n  }\n  componentDidMount() {\n    console.log('did mount');\n  }\n  componentWillUnmount() {\n    console.log('will unmount');\n  }\n  testFunc() {\n    console.log('test func');\n  }\n  onClick() {\n    this.dataSourceMap['info'].load(\n      { id: 1 }\n    )\n  }\n  onClick_new() {\n    this.dataSourceMap['infoList'].load(\n      { id: 1 }\n    )\n  }\n}",
      "hidden": false,
      "title": "dashboard",
      "isLocked": false,
      "condition": true,
      "meta": {
        "router": "/dashboard"
      },
      "conditionGroup": "",
      "children": [
        {
          "componentName": "Button",
          "id": "node_ocldwi9tvv1",
          "props": {
            "type": "primary",
            "children": "页面数据",
            "__component_name": "Button",
            "htmlType": "button",
            "size": "middle",
            "shape": "default",
            "icon": {
              "type": "JSSlot",
              "value": [
                {
                  "componentName": "Icon",
                  "id": "node_ocldwi9tvv3",
                  "props": {
                    "type": "SmileOutlined",
                    "size": 20,
                    "rotate": 0,
                    "spin": false,
                    "__component_name": "Icon"
                  },
                  "hidden": false,
                  "title": "",
                  "isLocked": false,
                  "condition": true,
                  "conditionGroup": ""
                }
              ]
            },
            "block": false,
            "danger": false,
            "ghost": false,
            "disabled": false,
            "__events": {
              "eventDataList": [
                {
                  "type": "componentEvent",
                  "name": "onClick",
                  "relatedEventName": "onClick"
                }
              ],
              "eventList": [
                {
                  "name": "onClick",
                  "template": "onClick(event,${extParams}){\n// 点击按钮时的回调\nconsole.log('onClick', event);}",
                  "disabled": true
                }
              ]
            },
            "onClick": {
              "type": "JSFunction",
              "value": "function(){return this.onClick.apply(this,Array.prototype.slice.call(arguments).concat([])) }"
            }
          },
          "hidden": false,
          "title": "",
          "isLocked": false,
          "condition": true,
          "conditionGroup": ""
        },
        {
          "componentName": "Button",
          "id": "node_ocldwi9u322",
          "props": {
            "type": "primary",
            "children": "公共数据源",
            "__component_name": "Button",
            "htmlType": "button",
            "size": "middle",
            "shape": "default",
            "icon": {
              "type": "JSSlot",
              "value": [
                {
                  "componentName": "Icon",
                  "id": "node_ocldwi9u325",
                  "props": {
                    "type": "SmileOutlined",
                    "size": 20,
                    "rotate": 0,
                    "spin": false,
                    "__component_name": "Icon"
                  },
                  "hidden": false,
                  "title": "",
                  "isLocked": false,
                  "condition": true,
                  "conditionGroup": ""
                }
              ]
            },
            "block": false,
            "danger": false,
            "ghost": false,
            "disabled": false,
            "__events": {
              "eventDataList": [
                {
                  "type": "componentEvent",
                  "name": "onClick",
                  "relatedEventName": "onClick_new"
                }
              ],
              "eventList": [
                {
                  "name": "onClick",
                  "template": "onClick(event,${extParams}){\n// 点击按钮时的回调\nconsole.log('onClick', event);}",
                  "disabled": true
                }
              ]
            },
            "onClick": {
              "type": "JSFunction",
              "value": "function(){return this.onClick_new.apply(this,Array.prototype.slice.call(arguments).concat([])) }"
            },
            "style": {
              "marginLeft": "10px"
            }
          },
          "hidden": false,
          "title": "",
          "isLocked": false,
          "condition": true,
          "conditionGroup": ""
        }
      ]
    }
  ],
  "i18n": {},
  "constants": {
    "ENV": "prod",
    "DOMAIN": "xxx.com"
  },
  "dataSource": {
    "list": [
      {
        "type": "fetch",
        "isInit": false,
        "options": {
          "params": {},
          "method": "GET",
          "isCors": true,
          "timeout": 5000,
          "headers": {},
          "uri": "mock/info.json"
        },
        "id": "infoList"
      }
    ]
  }
}
```

## 本地缓存

### antd-pro-with-formily:projectSchema

```
{"version":"1.0.0","componentsMap":[{"package":"@alilc/antd-lowcode-materials","version":"1.1.1","exportName":"Icon","main":"","destructuring":true,"componentName":"Icon"},{"package":"@alilc/antd-lowcode-materials","version":"1.1.1","exportName":"Button","main":"","destructuring":true,"componentName":"Button"},{"devMode":"lowCode","componentName":"Page"}],"componentsTree":[{"componentName":"Page","id":"node_dockcviv8fo1","props":{"ref":"outerView","style":{"height":"100%"}},"fileName":"/dashboard","dataSource":{"list":[{"type":"fetch","isInit":false,"options":{"params":{},"method":"GET","isCors":true,"timeout":5000,"headers":{},"uri":"mock/info.json"},"id":"info"}]},"state":{"text":{"type":"JSExpression","value":"\"outer\""},"isShowDialog":{"type":"JSExpression","value":"false"}},"css":"body {\n  font-size: 12px;\n}\n\n.button {\n  width: 100px;\n  color: #ff00ff\n}","lifeCycles":{"componentDidMount":{"type":"JSFunction","value":"function componentDidMount() {\n  console.log('did mount');\n}","source":"function componentDidMount() {\n  console.log('did mount');\n}"},"componentWillUnmount":{"type":"JSFunction","value":"function componentWillUnmount() {\n  console.log('will unmount');\n}","source":"function componentWillUnmount() {\n  console.log('will unmount');\n}"}},"methods":{"testFunc":{"type":"JSFunction","value":"function testFunc() {\n  console.log('test func');\n}","source":"function testFunc() {\n  console.log('test func');\n}"},"onClick":{"type":"JSFunction","value":"function onClick() {\n  this.dataSourceMap['info'].load({\n    id: 1\n  });\n}","source":"function onClick() {\n  this.dataSourceMap['info'].load({\n    id: 1\n  });\n}"},"onClick_new":{"type":"JSFunction","value":"function onClick_new() {\n  this.dataSourceMap['infoList'].load({\n    id: 1\n  });\n}","source":"function onClick_new() {\n  this.dataSourceMap['infoList'].load({\n    id: 1\n  });\n}"}},"originCode":"class LowcodeComponent extends Component {\n  state = {\n    \"text\": \"outer\",\n    \"isShowDialog\": false\n  }\n  componentDidMount() {\n    console.log('did mount');\n  }\n  componentWillUnmount() {\n    console.log('will unmount');\n  }\n  testFunc() {\n    console.log('test func');\n  }\n  onClick() {\n    this.dataSourceMap['info'].load(\n      { id: 1 }\n    )\n  }\n  onClick_new() {\n    this.dataSourceMap['infoList'].load(\n      { id: 1 }\n    )\n  }\n}","hidden":false,"title":"dashboard","isLocked":false,"condition":true,"meta":{"router":"/dashboard"},"conditionGroup":"","children":[{"componentName":"Button","id":"node_ocldwi9tvv1","props":{"type":"primary","children":"页面数据","__component_name":"Button","htmlType":"button","size":"middle","shape":"default","icon":{"type":"JSSlot","value":[{"componentName":"Icon","id":"node_ocldwi9tvv3","props":{"type":"SmileOutlined","size":20,"rotate":0,"spin":false,"__component_name":"Icon"},"hidden":false,"title":"","isLocked":false,"condition":true,"conditionGroup":""}]},"block":false,"danger":false,"ghost":false,"disabled":false,"__events":{"eventDataList":[{"type":"componentEvent","name":"onClick","relatedEventName":"onClick"}],"eventList":[{"name":"onClick","template":"onClick(event,${extParams}){\n// 点击按钮时的回调\nconsole.log('onClick', event);}","disabled":true}]},"onClick":{"type":"JSFunction","value":"function(){return this.onClick.apply(this,Array.prototype.slice.call(arguments).concat([])) }"}},"hidden":false,"title":"","isLocked":false,"condition":true,"conditionGroup":""},{"componentName":"Button","id":"node_ocldwi9u322","props":{"type":"primary","children":"公共数据源","__component_name":"Button","htmlType":"button","size":"middle","shape":"default","icon":{"type":"JSSlot","value":[{"componentName":"Icon","id":"node_ocldwi9u325","props":{"type":"SmileOutlined","size":20,"rotate":0,"spin":false,"__component_name":"Icon"},"hidden":false,"title":"","isLocked":false,"condition":true,"conditionGroup":""}]},"block":false,"danger":false,"ghost":false,"disabled":false,"__events":{"eventDataList":[{"type":"componentEvent","name":"onClick","relatedEventName":"onClick_new"}],"eventList":[{"name":"onClick","template":"onClick(event,${extParams}){\n// 点击按钮时的回调\nconsole.log('onClick', event);}","disabled":true}]},"onClick":{"type":"JSFunction","value":"function(){return this.onClick_new.apply(this,Array.prototype.slice.call(arguments).concat([])) }"},"style":{"marginLeft":"10px"}},"hidden":false,"title":"","isLocked":false,"condition":true,"conditionGroup":""}]}],"i18n":{}}
```


### antd-pro-with-formily:packages


```
[{"package":"moment","version":"2.24.0","urls":["https://g.alicdn.com/mylib/moment/2.24.0/min/moment.min.js"],"library":"moment"},{"package":"lodash","library":"_","urls":["https://g.alicdn.com/platform/c/lodash/4.6.1/lodash.min.js"]},{"package":"iconfont-icons","urls":"//at.alicdn.com/t/font_2369445_ukrtsovd92r.js"},{"package":"@ant-design/icons","version":"4.7.0","urls":["//g.alicdn.com/code/npm/@ali/ant-design-icons-cdn/4.5.0/index.umd.min.js"],"library":"icons"},{"package":"antd","version":"4.23.0","urls":["//g.alicdn.com/code/lib/antd/4.23.0/antd.min.js","//g.alicdn.com/code/lib/antd/4.23.0/antd.min.css"],"library":"antd"},{"title":"fusion组件库","package":"@alifd/next","version":"1.26.4","urls":["https://g.alicdn.com/code/lib/alifd__next/1.26.4/next.min.css","https://g.alicdn.com/code/lib/alifd__next/1.26.4/next-with-locales.min.js"],"library":"Next"},{"package":"@alilc/antd-lowcode-materials","version":"1.1.1","library":"AntdLowcode","urls":["https://alifd.alicdn.com/npm/@alilc/antd-lowcode-materials@1.1.1/build/lowcode/view.js","https://alifd.alicdn.com/npm/@alilc/antd-lowcode-materials@1.1.1/build/lowcode/view.css"],"editUrls":["https://alifd.alicdn.com/npm/@alilc/antd-lowcode-materials@1.1.1/build/lowcode/view.js","https://alifd.alicdn.com/npm/@alilc/antd-lowcode-materials@1.1.1/build/lowcode/view.css"]},{"package":"@seada/antd-materials","version":"1.0.0-rc.27","library":"SeadaAntdMaterials","urls":["https://unpkg.com/@seada/antd-materials@1.0.0-rc.27/build/lowcode/view.js","https://unpkg.com/@seada/antd-materials@1.0.0-rc.27/build/lowcode/view.css"],"editUrls":["https://unpkg.com/@seada/antd-materials@1.0.0-rc.27/build/lowcode/view.js","https://unpkg.com/@seada/antd-materials@1.0.0-rc.27/build/lowcode/view.css"]},{"package":"@seada/formily-materials","version":"1.0.0-rc.27","library":"SeadaFormilyMaterials","urls":["https://unpkg.com/@seada/formily-materials@1.0.0-rc.27/build/lowcode/view.js","https://unpkg.com/@seada/formily-materials@1.0.0-rc.27/build/lowcode/view.css"],"editUrls":["https://unpkg.com/@seada/formily-materials@1.0.0-rc.27/build/lowcode/view.js","https://unpkg.com/@seada/formily-materials@1.0.0-rc.27/build/lowcode/view.css"]}]

```









