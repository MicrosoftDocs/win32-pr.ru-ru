---
description: Указывает, что объект Шеллфолдервиев завершил перечисление содержимого папки.
title: Событие Шеллфолдервиевок. Енумдоне (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: c725a61a6711dab22d50b774cb02556916dae802a66008a48721d7311e163bce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660644"
---
# <a name="shellfolderviewocenumdone-event"></a>Шеллфолдервиевок. Енумдоне, событие

Указывает, что объект [**шеллфолдервиев**](shellfolderview.md) завершил перечисление содержимого папки.

## <a name="syntax"></a>Синтаксис


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a>Параметры

Этот обработчик событий не имеет параметров.

## <a name="remarks"></a>Remarks

Объект [**шеллфолдервиев**](shellfolderview.md) должен перечислить содержимое папки, прежде чем она сможет ее отобразить. При наличии больших или расположенных в удаленной системе папок Этот процесс может занять несколько минут. В течение этого времени отображается анимированный рисунок фонарик, указывающий пользователю, что обработка выполняется по-разному. После перечисления будет вызвано событие **енумдоне** , и изображение фонарик заменяется содержимым папки.

Укажите код обработки событий для этого события, как показано здесь.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**шеллфолдервиевок**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




