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
ms.openlocfilehash: 140fbdc79980a2ab6ba9f50b8815429436df0d3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143072"
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

## <a name="remarks"></a>Примечания

Значения *HWND* и **HMENU** , передаваемые с помощью [**фмевент \_ Load**](fmevent-load.md) и [**фмевент \_ инитмену**](fmevent-initmenu.md) messages, могут быть недействительны во время отправки этого сообщения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> </dl>

 

 




