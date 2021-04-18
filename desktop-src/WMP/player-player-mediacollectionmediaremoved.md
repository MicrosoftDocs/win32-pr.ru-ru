---
title: Событие Player. Медиаколлектионмедиаремовед
description: Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки. | Событие Player. Медиаколлектионмедиаремовед
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Проигрыватель Windows Media Event Медиаколлектионмедиаремовед
- Проигрыватель Windows Media Event Медиаколлектионмедиаремовед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионмедиаремовед
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
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708593"
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

## <a name="remarks"></a>Комментарии

Это событие происходит только в локальной библиотеке.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Медиаколлектион**](player-mediacollection.md)
</dt> </dl>

 

 





