---
title: Ошибка. метод Клеарерроркуеуе
description: Метод Клеарерроркуеуе удаляет ошибки из очереди ошибок. | Ошибка. метод Клеарерроркуеуе
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- Клеарерроркуеуе метод Windows Media Player
- метод Клеарерроркуеуе Windows Media Player, класс Error
- Класс ошибок Windows Media Player, метод Клеарерроркуеуе
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694925"
---
# <a name="errorclearerrorqueue-method"></a>Ошибка. метод Клеарерроркуеуе

Метод **клеарерроркуеуе** удаляет ошибки из очереди ошибок.

## <a name="syntax"></a>Синтаксис


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод полезен для очистки очереди ошибок после обработки ряда ошибок.

Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Ошибка*. **клеарерроркуеуе** в обработчике событий, чтобы очистить очередь ошибок после отображения всех описаний ошибок. Объект **Player** создан с идентификатором "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Error**](error-object.md)
</dt> </dl>

 

 





