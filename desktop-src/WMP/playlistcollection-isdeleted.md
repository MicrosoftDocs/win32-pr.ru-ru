---
title: Плайлистколлектион. isDeleted, метод
description: Метод IsDeleted извлекает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- метод IsDeleted Windows Media Player
- метод IsDeleted Windows Media Player, класс Плайлистколлектион
- Класс Плайлистколлектион Windows Media Player, метод isDeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717965"
---
# <a name="playlistcollectionisdeleted-method"></a>Плайлистколлектион. isDeleted, метод

Метод **IsDeleted** извлекает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.

## <a name="syntax"></a>Синтаксис


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*список воспроизведения* \[ окне\]
</dt> <dd>

Искомый объект **списка воспроизведения** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **логическое значение**.

**Проигрыватель Windows Media 10 Mobile**: Этот метод всегда возвращает **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0, Windows Media Player версии 7,1 или Windows Media Player для Windows XP. Этот метод не поддерживается для серии проигрывателя Windows Media 9 или более поздней версии.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Плайлистколлектион**](playlistcollection-object.md)
</dt> </dl>

 

 





