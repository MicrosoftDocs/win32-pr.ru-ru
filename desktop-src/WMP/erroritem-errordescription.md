---
title: Ерроритем. errorDescription
description: Свойство errorDescription Извлекает описание ошибки.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- Проигрыватель Windows Media Ерроритем. errorDescription
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694534"
---
# <a name="erroritemerrordescription"></a>Ерроритем. errorDescription

Свойство **errorDescription** Извлекает описание ошибки.

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой**, доступная только для чтения.

## <a name="remarks"></a>Комментарии

Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *ерроритем*. **errorDescription** в обработчике событий для вывода сообщения об ошибке пользователю. Объект **Player** создан с идентификатором "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> </dl>

 

 





