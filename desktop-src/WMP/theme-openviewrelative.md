---
title: THEME. Опенвиеврелативе
description: Метод Опенвиеврелативе открывает представление в новом окне с указанной начальной позицией относительно левого верхнего угла обложки.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- проигрыватель Windows Media THEME. опенвиеврелативе
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a26040bb8f47d85be99f0d8df602bdd69835cfa648ac6d5898f786e4518acdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117778"
---
# <a name="themeopenviewrelative"></a>THEME. Опенвиеврелативе

Метод **опенвиеврелативе** открывает **представление** в новом окне с указанной начальной позицией относительно левого верхнего угла обложки.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*режиме*
</dt> <dd>

**Строка** , указывающая **идентификатор** открываемого **представления** .

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*слева*
</dt> <dd>

**Число** (**длинное**), определяющее начальное расстояние в пикселях от левой границы **представления** до левого края обложки. Отрицательное значение указывает на начальную точку слева от границы обложки.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*Вверх*
</dt> <dd>

**Число** (**длинное**), указывающее начальное расположение верхней границы **представления** относительно верхней границы обложки. Отрицательные значения указывают начальную точку над границей обложки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Позиция, указанная для **представления** , используется при первом вызове этого метода, после чего пользователь может перетащить **представление** в другое место. Новая заданная позицией сохраняется, и при последующих вызовах используется самая последняя.

## <a name="examples"></a>Примеры


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> <dt>

[**THEME. closeView**](theme-closeview.md)
</dt> <dt>

[**THEME. openView**](theme-openview.md)
</dt> </dl>

 

 





