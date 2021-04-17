---
title: Controls. Куррентпоситионстринг
description: Свойство Куррентпоситионстринг извлекает текущую позицию в элементе мультимедиа в виде строки в формате чч мм СС (часы, минуты и секунды).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Проигрыватель Windows Media Controls. Куррентпоситионстринг
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
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698991"
---
# <a name="controlscurrentpositionstring"></a>Controls. Куррентпоситионстринг

Свойство **куррентпоситионстринг** извлекает текущую позицию в элементе мультимедиа в виде **строки** , отформатированной как чч: мм: СС (часы, минуты и секунды).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой**, доступная только для чтения.

## <a name="remarks"></a>Комментарии

Если размер элемента мультимедиа меньше часа, часть чч: не включается.

> [!Note]  
> Необходимо включить код для остановки таймера при остановке или приостановке элемента мультимедиа.

 

## <a name="examples"></a>Примеры

В следующем примере JScript запускается таймер HTML, который отображает текущее расположение файла мультимедиа с интервалом в 1 секунду. Для вывода текущей позицией был создан HTML-элемент с именем MyText. Объект **Player** создан с идентификатором "Player".


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> </dl>

 

 





