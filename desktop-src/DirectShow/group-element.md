---
description: Элемент Group определяет группу, объект верхнего уровня на временной шкале.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Элемент Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eda120363540eaf467ebb9beaea4705c4b430077c55b5b05c46197d90920b40a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997835"
---
# <a name="group-element"></a>Group, элемент

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Элемент **Group** определяет группу, объект верхнего уровня на временной шкале.

## <a name="attributes"></a>Атрибуты

[**битдепс**](bitdepth-attribute.md), [**буферизация**](buffering-attribute.md), [**Частота кадров**](framerate-attribute.md), [**Высота**](height-attribute.md), [**Блокировка**](lock-attribute.md), [**Отключение звука**](mute-attribute.md), [**имя**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**самплинграте**](samplingrate-attribute.md), [**тип**](type-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md), [**Ширина**](width-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



| Метка | Значение |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**графика**](timeline-element.md)                                                                     |
| Дети | [**составной**](composite-element.md), [**результат**](effect-element.md), [**трекинг**](track-element.md) |



 

## <a name="remarks"></a>Remarks

В пределах `group` элемента приоритет вложенных слоев определяется неявно в порядке их расположения в элементе. Первый уровень имеет приоритет 0, а последующие уровни увеличивают значения приоритета.

## <a name="examples"></a>Примеры


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 



