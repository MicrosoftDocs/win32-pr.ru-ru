---
title: ПОЛЗУНок. Фореграундпрогресс
description: Атрибут Фореграундпрогресс указывает или получает текущую положение индикатора выполнения на передний план в процентах от области ползунка.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- ПОЛЗУНок. Фореграундпрогресс Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657722"
---
# <a name="sliderforegroundprogress"></a>ПОЛЗУНок. Фореграундпрогресс

Атрибут **фореграундпрогресс** указывает или получает текущую положение индикатора выполнения на передний план в процентах от области ползунка.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) в диапазоне от 0 до 100.

## <a name="remarks"></a>Комментарии

Этот атрибут используется в основном для отслеживания хода загрузки файла мультимедиа при одновременной отслеживании текущей позицией воспроизведения файла с помощью атрибута **value** . Положение ползунка ограничивается областью выполнения переднего плана. Это позволяет интерактивному поиску выполняться только в пределах доступной части загружаемого файла.

Для использования этой функции атрибут **усефореграундпрогресс** должен иметь значение true.

## <a name="examples"></a>Примеры


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. min**](slider-min.md)
</dt> <dt>

[**SLIDER. Max**](slider-max.md)
</dt> <dt>

[**ПОЛЗУНок. Усефореграундпрогресс**](slider-useforegroundprogress.md)
</dt> <dt>

[**ПОЛЗУНок. Value**](slider-value.md)
</dt> </dl>

 

 





