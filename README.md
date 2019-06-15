# idea-settings
idea默认配置

主要是code templates和live templates
### 方法签名
方法签名

``` groovy
# 参数
groovyScript("if(\"${_1}\".length() == 2) {return '';} else {def result=''; def params=\"${_1}\".replaceAll('[\\\\[|\\\\]|\\\\s]', '').split(',').toList();for(i = 0; i < params.size(); i++) {if(i<(params.size()-1)){result+=' * @param ' + params[i] + ' : ' + '\\n'}else{result+=' * @param ' + params[i] + ' : '}}; return result;}", methodParameters()); 


# 返回值

groovyScript("def returnType = \"${_1}\"; def result = ' * @return  ' + returnType; return result;", methodReturnType());
```