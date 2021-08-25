---
title: Ерроритем. errorDescription
description: Свойство errorDescription Извлекает описание ошибки.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ерроритем. errorDescription проигрыватель Windows Media
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
ms.openlocfilehash: c5740adcef0b6eb86290ea392d0659abb0ccc3d51b0b0b1b3203105de67fb692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862794"
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

## <a name="remarks"></a>Remarks

необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *ерроритем*. **errorDescription** в обработчике событий для вывода сообщения об ошибке пользователю. Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> </dl>

 

 





