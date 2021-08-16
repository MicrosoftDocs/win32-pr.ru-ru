---
title: Событие Player. Плайлистколлектионплайлистремовед
description: Событие Плайлистколлектионплайлистремовед возникает при удалении списка воспроизведения из коллекции списков воспроизведения. | Событие Player. Плайлистколлектионплайлистремовед
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- проигрыватель Windows Media событий плайлистколлектионплайлистремовед
- проигрыватель Windows Media событий плайлистколлектионплайлистремовед, класс Player
- класс проигрывателя проигрыватель Windows Media, событие плайлистколлектионплайлистремовед
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 456f7598b9e1f1d2c2a6e76e58a0b06142980835c3c6d71d9ab10c2230ac386f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118337978"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Событие Player. Плайлистколлектионплайлистремовед

Событие **плайлистколлектионплайлистремовед** возникает при удалении списка воспроизведения из коллекции списков воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрплайлистнаме* 
</dt> <dd>

**Строка** , указывающая имя списка воспроизведения, который был удален.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Плайлистколлектион. Жетбинаме**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





