## TWIG 模板引擎

#### 获取 request 中的get信息
	 {{ app.requet.get('parameter_name') }}

#### 控制文本内容
	{{ c.title|length > 50 ? c.title|slice(0, 50) ~ '...' :c.title  }}
	{{ istr.informantSituation|truncate(12,false,'...')|default('暂无数据') }}

#### 数组转字符串
	{{ $arr|join('$glue') }}

####获取路由名称
	{{ app.request.get('_route') }}

#### 处理日期  
	{{ time|date("m月d日  周D")|replace({'Mon':'一','Tue':'二','Wed':'三','Thu':'四','Fri':'五','Sat':'六','Sun':'日'}) }}   周处理

#### 获取数组长度 （用于统计数组）
	{{ arr|length }}