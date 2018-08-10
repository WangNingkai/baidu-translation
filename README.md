百度翻译API封装
==================

[![Latest Stable Version](https://poser.pugx.org/wangningkai/baidu-translation/v/stable)](https://packagist.org/packages/wangningkai/baidu-translation)
[![Total Downloads](https://poser.pugx.org/wangningkai/baidu-translation/downloads)](https://packagist.org/packages/wangningkai/baidu-translation)
[![Latest Unstable Version](https://poser.pugx.org/wangningkai/baidu-translation/v/unstable)](https://packagist.org/packages/wangningkai/baidu-translation)
[![License](https://poser.pugx.org/wangningkai/baidu-translation/license)](https://packagist.org/packages/wangningkai/baidu-translation)

### Usage:

- 定位到您的项目路径运行

```
composer require wangningkai/laravel-baidu-translation
```

```php

    use WangNingkai\Translation\BaiduTranslation;
    
    # $app_id = 您的ID;
    # $secrect_key = 您的Key;

    $translation = new BaiduTranslation($app_id,$secrect_key);

    # $query 要查询的内容
    # $from 源语言（见语言列表）
    # $to 目标语言 （见语言列表）


    $res = $translation->translate($query,$from,$to);

```

返回值为json格式

```json
成功：
{
    'result':'翻译结果',
    'status': 0
}

失败：
{
    'result':'错误原因',
    'status': 1
}
```

#### 语言列表
```
    # 语言简写	    名称
    # auto	      自动检测
    # zh	       中文
    # en	       英语
    # yue	       粤语
    # wyw	       文言文
    # jp	       日语
    # kor	       韩语
    # fra	       法语
    # spa	       西班牙语
    # th	       泰语
    # ara	       阿拉伯语
    # ru	       俄语
    # pt	       葡萄牙语
    # de	       德语
    # it	       意大利语
    # el	       希腊语
    # nl	       荷兰语
    # pl	       波兰语
    # bul	       保加利亚语
    # est	       爱沙尼亚语
    # dan	       丹麦语
    # fin	       芬兰语
    # cs	       捷克语
    # rom	       罗马尼亚语
    # slo	       斯洛文尼亚语
    # swe	       瑞典语
    # hu	       匈牙利语
    # cht	       繁体中文
    # vie	       越南语
```
