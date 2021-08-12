---
title: Событие Player. Медиаеррор
description: Событие Медиаеррор возникает, когда объект мультимедиа имеет условие ошибки.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- проигрыватель Windows Media событий медиаеррор
- проигрыватель Windows Media событий медиаеррор, класс Player
- класс проигрывателя проигрыватель Windows Media, событие медиаеррор
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
ms.openlocfilehash: cb1eb94d245f0b0a91786b2b1a7b677429cc9040d8cbb1372164bf6e7ed209d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572844"
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

## <a name="remarks"></a>Remarks

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media для Windows XP или более поздней версии.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





