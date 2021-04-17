---
title: Просмотр. размер
description: Метод size изменяет размер представления на указанном крае.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- Просмотр. Размер проигрывателя Windows Media
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704180"
---
# <a name="viewsize"></a>Просмотр. размер

Метод **size** изменяет размер **представления** на указанном крае.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*справиться*
</dt> <dd>

Строка, указывающая ребро или угол для перемещения при изменении размера. Эта строка должна иметь одно из следующих восьми значений.



| Edge   | Угол      |
|--------|-------------|
| top    | верхнем    |
| right  | боттомригхт |
| снизу | боттомлефт  |
| Левое   | топлефт     |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод обычно вызывается из обработчика **OnMouseDown** . Он занимается изменением размера при перетаскивании мыши и прекращает изменение размера при отпускании кнопки мыши. Если размер **представления** ограничен, нельзя перетаскивать указатель мыши, чтобы изменить размер **представления** за пределами ограниченных границ.

## <a name="examples"></a>Примеры


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**VIEW, элемент**](view-element.md)
</dt> </dl>

 

 





