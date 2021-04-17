---
title: ЕКУАЛИЗЕРСЕТТИНГС. Гаинлевелс
description: Атрибут Гаинлевелс указывает или получает уровень усиления диапазона, соответствующий указанному индексу.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- Проигрыватель Windows Media ЕКУАЛИЗЕРСЕТТИНГС. Гаинлевелс
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694782"
---
# <a name="equalizersettingsgainlevels"></a>ЕКУАЛИЗЕРСЕТТИНГС. Гаинлевелс

Атрибут **гаинлевелс** указывает или получает уровень усиления диапазона, соответствующий указанному индексу.

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) со значением, которое обычно находится в диапазоне от 20 до + 20.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*себанд*
</dt> <dd>

**Число**(**Long**) от 1 до 10, указывающее индекс полосы.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот атрибут принимает параметр, но его значение указывается в коде скрипта так же, как и другие значения атрибутов. Он не может быть указан в элементе ЕКУАЛИЗЕРСЕТТИНГС и не может использоваться с атрибутом прослушивания **вмппроп** . Вместо этого для таких ситуаций предоставляются пронумерованные атрибуты уровня прибыли.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**Атрибуты прослушивания**](listening-attributes.md)
</dt> </dl>

 

 





