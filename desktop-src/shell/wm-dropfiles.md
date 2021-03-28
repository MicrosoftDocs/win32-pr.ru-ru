---
description: Посылается, когда пользователь удаляет файл в окне приложения, которое зарегистрировалось как получатель удаленных файлов.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Сообщение WM_DROPFILES (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985393"
---
# <a name="wm_dropfiles-message"></a>\_Сообщение ДРОПФИЛЕС WM

Посылается, когда пользователь удаляет файл в окне приложения, которое зарегистрировалось как получатель удаленных файлов.


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*hDrop* 
</dt> <dd>

Маркер внутренней структуры, описывающей удаленные файлы. Передайте этот обработчик [**драгфиниш**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**драгкуерифиле**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)или [**драгкуерипоинт**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) , чтобы получить сведения об удаленных файлах.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Примечания

Маркер HDROP объявляется в Шеллапи. h. Этот заголовок необходимо включить в сборку для использования **WM \_ дропфилес**. Более подробное обсуждение того, как использовать перетаскивание для передачи данных оболочки, см. в разделе [Передача данных оболочки с помощью перетаскивания или буфера обмена](dragdrop.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**DragAcceptFiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
