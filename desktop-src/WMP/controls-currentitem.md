---
title: Controls. currentItem
description: Свойство currentItem указывает или получает текущий элемент мультимедиа.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- controls. currentItem проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dc0ad047213e0fbba7dbdd7336e67b8d015e39aba510ac37bd3701462413ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997555"
---
# <a name="controlscurrentitem"></a>Controls. currentItem

Свойство **currentItem** указывает или получает текущий элемент мультимедиа.

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является объектом **мультимедиа** для чтения и записи.

## <a name="remarks"></a>Remarks

Этот метод работает только с элементами в *проигрывателе*. **куррентплайлист**. Вызов **currentItem** со ссылкой на сохраненный элемент мультимедиа не поддерживается.

## <a name="examples"></a>Примеры

в следующем примере JScript используется **currentItem** , чтобы задать для текущего элемента управления "проигрыватель" значение, выбранное в HTML-элементе SELECT. Текущий список воспроизведения был впервые указан с помощью *плайлистколлектион*. **жетбинаме**. Объект **Player** создан с идентификатором "Player".


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Плайлистколлектион. Жетбинаме**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





