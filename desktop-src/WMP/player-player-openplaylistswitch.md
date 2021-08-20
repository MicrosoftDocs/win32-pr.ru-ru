---
title: Событие Player. Опенплайлистсвитч
description: Событие Опенплайлистсвитч возникает, когда начинается воспроизведение заголовка на DVD-диске. | Событие Player. Опенплайлистсвитч
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- проигрыватель Windows Media событий опенплайлистсвитч
- проигрыватель Windows Media событий опенплайлистсвитч, класс Player
- класс проигрывателя проигрыватель Windows Media, событие опенплайлистсвитч
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5610c4e5a4870b1ad5dc5d12d9d8c315dce630578d5af01f8f428b1af47884e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835151"
---
# <a name="playeropenplaylistswitch-event"></a>Событие Player. Опенплайлистсвитч

Событие **опенплайлистсвитч** возникает, когда начинается воспроизведение заголовка на DVD-диске.

## <a name="syntax"></a>Синтаксис


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*питем* 
</dt> <dd>

Объект **списка воспроизведения** , представляющий заголовок.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media для Windows XP или более поздней версии.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





