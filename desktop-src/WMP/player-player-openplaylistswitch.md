---
title: Событие Player. Опенплайлистсвитч
description: Событие Опенплайлистсвитч возникает, когда начинается воспроизведение заголовка на DVD-диске. | Событие Player. Опенплайлистсвитч
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Проигрыватель Windows Media Event Опенплайлистсвитч
- Проигрыватель Windows Media Event Опенплайлистсвитч, класс Player
- Класс проигрывателя Windows Media Player, событие Опенплайлистсвитч
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
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704243"
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

## <a name="remarks"></a>Комментарии

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





