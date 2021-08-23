---
title: ПОЛЗУНок. Фореграундпрогресс
description: Атрибут Фореграундпрогресс указывает или получает текущую положение индикатора выполнения на передний план в процентах от области ползунка.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- проигрыватель Windows Media SLIDER. фореграундпрогресс
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48819a2b3245fc8a72d29e9a30135cc37702417ca498c88b8be01578b74988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646344"
---
# <a name="sliderforegroundprogress"></a>ПОЛЗУНок. Фореграундпрогресс

Атрибут **фореграундпрогресс** указывает или получает текущую положение индикатора выполнения на передний план в процентах от области ползунка.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) в диапазоне от 0 до 100.

## <a name="remarks"></a>Remarks

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

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

 

 





