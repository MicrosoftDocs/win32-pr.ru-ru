---
title: Ошибка. Ерроркаунт
description: Свойство Ерроркаунт извлекает количество ошибок в очереди ошибок.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Ошибка. Ерроркаунт Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694515"
---
# <a name="errorerrorcount"></a>Ошибка. Ерроркаунт

Свойство **ерроркаунт** извлекает количество ошибок в очереди ошибок.

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Ошибка*. **ерроркаунт** в обработчике событий, чтобы предупредить пользователя о последней ошибке в очереди ошибок. Объект **Player** создан с идентификатором "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

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

[**Объект Error**](error-object.md)
</dt> </dl>

 

 





