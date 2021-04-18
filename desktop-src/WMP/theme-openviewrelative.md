---
title: THEME. Опенвиеврелативе
description: Метод Опенвиеврелативе открывает представление в новом окне с указанной начальной позицией относительно левого верхнего угла обложки.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- Проигрыватель Windows Media THEME. Опенвиеврелативе
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675559"
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

## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент THEME**](theme-element.md)
</dt> <dt>

[**THEME. closeView**](theme-closeview.md)
</dt> <dt>

[**THEME. openView**](theme-openview.md)
</dt> </dl>

 

 





