---
title: Событие Player. Error
description: Событие ошибки возникает при возникновении состояния ошибки.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Проигрыватель Windows Media, событие ошибки
- Событие ошибки Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, событие ошибки
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708316"
---
# <a name="playererror-event"></a>Событие Player. Error

Событие **ошибки** возникает при возникновении состояния ошибки.

## <a name="syntax"></a>Синтаксис


```JScript
Player.Error()
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="examples"></a>Примеры

В следующем примере JScript создается обработчик событий для вывода текста описания первой ошибки в очереди ошибок. Объект **Player** создан с идентификатором "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ерроритем. errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Ошибка. элемент**](error-item.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





