# think-smarty
ThinkPHP5.1Smarty 引擎驱动

## 安装方法

使用composer安装模版引擎方法: `composer require yaofulai/think-smarty`

## ThinkPHP5.1 配置template.php文件中参数

```
return [
    // 模板引擎类型 支持 php think 支持扩展
    'type'         => 'Smarty',
    // 默认模板渲染规则 1 解析为小写+下划线 2 全部转换小写 3 保持操作方法
    'auto_rule'    => 1,
    // 模板路径
    'view_path'    => '',
    // 模板后缀
    'view_suffix'  => 'html',
    // 模板文件名分隔符
    'view_depr'    => '_', //DIRECTORY_SEPARATOR,
    // 模板引擎普通标签开始标记
    'tpl_begin'    => '<{',
    // 模板引擎普通标签结束标记
    'tpl_end'      => '}>',
    // 标签库标签开始标记
    'taglib_begin' => '{',
    // 标签库标签结束标记
    'taglib_end'   => '}', 

	'view_replace_str'  =>  [   //字符替换部分
        '/Upfiles/'=>'http://img.qudian.com/Uploads/',
   ], 

];
```
那么在控制器 `index/index::index` 中 `return view();`时会加载模板 `index/view/index_index.html``
