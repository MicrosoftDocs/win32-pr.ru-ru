---
title: Событие Player. Куррентплайлистчанже
description: Событие Куррентплайлистчанже возникает при изменении в текущем списке воспроизведения. | Событие Player. Куррентплайлистчанже
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- проигрыватель Windows Media событий куррентплайлистчанже
- проигрыватель Windows Media событий куррентплайлистчанже, класс Player
- класс проигрывателя проигрыватель Windows Media, событие куррентплайлистчанже
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672ff739e60efe73e1d30670dec5bc956f9fdd56506464b036add6f52cc6fc34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338150"
---
# <a name="playercurrentplaylistchange-event"></a>Событие Player. Куррентплайлистчанже

Событие **куррентплайлистчанже** возникает при изменении в текущем списке воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*change* 
</dt> <dd>

**Число** (**длинное**), указывающее тип изменений, произошедших в списке воспроизведения. См. *проигрыватель*. Событие **плайлистчанже** для таблицы возможных значений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Это событие не происходит, если другой список воспроизведения попадает в текущий список воспроизведения. Это происходит только в том случае, если изменение происходит в текущем списке воспроизведения, например при добавлении элемента мультимедиа в список воспроизведения.

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

## <a name="examples"></a>Примеры

следующий пример JScript обновляет текст в элементе HTML DIV с именем плитемс, чтобы отобразить имена элементов мультимедиа в текущем списке воспроизведения. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Куррентплайлист**](player-currentplaylist.md)
</dt> <dt>

[**Player. Плайлистчанже**](player-player-playlistchange.md)
</dt> </dl>

 

 





