---
description: Отправляется в библиотеку DLL расширения, когда диспетчер файлов выгружает библиотеку DLL.
title: Сообщение FMEVENT_UNLOAD (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 24b5b2a77393178cad545cb63c1524a8d7e92c5c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843075"
---
# <a name="fmevent_unload-message"></a>\_Сообщение о выгрузке фмевент

Отправляется в библиотеку DLL расширения, когда диспетчер файлов выгружает библиотеку DLL.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Библиотека DLL расширения должна вернуть нуль, если обрабатывает это сообщение.

## <a name="remarks"></a>Remarks

Значения *HWND* и **HMENU** , передаваемые с помощью [**фмевент \_ Load**](fmevent-load.md) и [**фмевент \_ инитмену**](fmevent-initmenu.md) messages, могут быть недействительны во время отправки этого сообщения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> </dl>

 

 




