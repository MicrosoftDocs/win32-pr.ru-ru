---
title: Событие Player. Медиаколлектионмедиаремовед
description: Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки. | Событие Player. Медиаколлектионмедиаремовед
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- проигрыватель Windows Media событий медиаколлектионмедиаремовед
- проигрыватель Windows Media событий медиаколлектионмедиаремовед, класс Player
- класс проигрывателя проигрыватель Windows Media, событие медиаколлектионмедиаремовед
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009432040deace140dd3cf4d7d7da1246c0a38dbd9fc0da028832af137cefa83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572854"
---
# <a name="playermediacollectionmediaremoved-event"></a>Событие Player. Медиаколлектионмедиаремовед

Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки.

## <a name="syntax"></a>Синтаксис


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдиспмедиа* 
</dt> <dd>

Удаленный объект **мультимедиа** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Это событие происходит только в локальной библиотеке.

**проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Медиаколлектион**](player-mediacollection.md)
</dt> </dl>

 

 





