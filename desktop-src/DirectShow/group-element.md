---
description: Элемент Group определяет группу, объект верхнего уровня на временной шкале.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Элемент Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990255"
---
# <a name="group-element"></a>Group, элемент

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Элемент **Group** определяет группу, объект верхнего уровня на временной шкале.

## <a name="attributes"></a>Атрибуты

[**битдепс**](bitdepth-attribute.md), [**буферизация**](buffering-attribute.md), [**Частота кадров**](framerate-attribute.md), [**Высота**](height-attribute.md), [**Блокировка**](lock-attribute.md), [**Отключение звука**](mute-attribute.md), [**имя**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**самплинграте**](samplingrate-attribute.md), [**тип**](type-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md), [**Ширина**](width-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**графика**](timeline-element.md)                                                                     |
| Дети | [**составной**](composite-element.md), [**результат**](effect-element.md), [**трекинг**](track-element.md) |



 

## <a name="remarks"></a>Комментарии

В пределах `group` элемента приоритет вложенных слоев определяется неявно в порядке их расположения в элементе. Первый уровень имеет приоритет 0, а последующие уровни увеличивают значения приоритета.

## <a name="examples"></a>Примеры


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 



