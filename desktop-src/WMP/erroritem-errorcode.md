---
title: Ерроритем. errorCode
description: Свойство errorCode извлекает текущий код ошибки.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- Ерроритем. errorCode проигрыватель Windows Media
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694536"
---
# <a name="erroritemerrorcode"></a>Ерроритем. errorCode

Свойство **ErrorCode** извлекает текущий код ошибки.

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *ерроритем*. **ErrorCode** в обработчике событий для вывода кода ошибки пользователю. Объект **Player** создан с идентификатором "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> <dt>

[**Ерроритем. errorDescription**](erroritem-errordescription.md)
</dt> </dl>

 

 





