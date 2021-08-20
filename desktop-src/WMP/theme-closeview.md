---
title: THEME. closeView
description: Метод closeView закрывает открытое представление.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- проигрыватель Windows Media THEME. closeView
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e66a0c56ab2f5fc3d5d6a27d996d8b3f3cf7834c61e62113a40af3c42aeb4d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932549"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> <dt>

[**THEME. openView**](theme-openview.md)
</dt> </dl>

 

 





