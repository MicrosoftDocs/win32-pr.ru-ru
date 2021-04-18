---
title: THEME. closeView
description: Метод closeView закрывает открытое представление.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- Проигрыватель Windows Media THEME. closeView
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648652"
---
# <a name="themecloseview"></a>THEME. closeView

Метод **closeView** закрывает открытое **представление**.

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*севиев*
</dt> <dd>

**Строка** , указывающая **идентификатор** закрытого **представления** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> <dt>

[**THEME. openView**](theme-openview.md)
</dt> </dl>

 

 





