---
description: Указывает, что состояние выбора одного или нескольких элементов в представлении изменилось.
title: Событие Шеллфолдервиевок. SelectionChanged (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 264631c43dd9ac20bd0ae47632738c2a37a0a85168b487e17ff86a8a2b71c8ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660634"
---
# <a name="shellfolderviewocselectionchanged-event"></a>Шеллфолдервиевок. SelectionChanged, событие

Указывает, что состояние выбора одного или нескольких элементов в представлении изменилось.

## <a name="syntax"></a>Синтаксис


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>Параметры

Этот обработчик событий не имеет параметров.

## <a name="remarks"></a>Remarks

Укажите код обработки событий для этого события, как показано здесь.


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**шеллфолдервиевок**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




