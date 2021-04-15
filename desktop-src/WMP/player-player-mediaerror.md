---
title: Событие Player. Медиаеррор
description: Событие Медиаеррор возникает, когда объект мультимедиа имеет условие ошибки.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Проигрыватель Windows Media Event Медиаеррор
- Проигрыватель Windows Media Event Медиаеррор, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаеррор
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708359"
---
# <a name="playermediaerror-event"></a>Событие Player. Медиаеррор

Событие **медиаеррор** возникает, когда объект **мультимедиа** имеет условие ошибки.

## <a name="syntax"></a>Синтаксис


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиаобжект* 
</dt> <dd>

Объект **мультимедиа** с условием ошибки.

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

 

 





