---
title: Controls. Куррентпоситионстринг
description: Свойство Куррентпоситионстринг извлекает текущую позицию в элементе мультимедиа в виде строки в формате чч мм СС (часы, минуты и секунды).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- controls. куррентпоситионстринг проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 640f0f97e3fa4c4054df17ea92304ad7721c770d9cb9b56436dcf810b9c083ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651994"
---
# <a name="controlscurrentpositionstring"></a>Controls. Куррентпоситионстринг

Свойство **куррентпоситионстринг** извлекает текущую позицию в элементе мультимедиа в виде **строки** , отформатированной как чч: мм: СС (часы, минуты и секунды).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой**, доступная только для чтения.

## <a name="remarks"></a>Remarks

Если размер элемента мультимедиа меньше часа, часть чч: не включается.

> [!Note]  
> Необходимо включить код для остановки таймера при остановке или приостановке элемента мультимедиа.

 

## <a name="examples"></a>Примеры

в следующем примере JScript запускается таймер HTML, отображающий текущее расположение файла мультимедиа с интервалом в 1 секунду. Для вывода текущей позицией был создан HTML-элемент с именем MyText. Объект **Player** создан с идентификатором "Player".


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> </dl>

 

 





