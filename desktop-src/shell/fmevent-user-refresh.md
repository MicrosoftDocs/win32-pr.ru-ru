---
description: Отправляется в библиотеку DLL расширения, когда пользователь выбирает команду "Обновить" из меню "вид" в диспетчере файлов. Расширение может использовать это уведомление для обновления меню.
title: Сообщение FMEVENT_USER_REFRESH (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: c3c4596b0ea589545c6e59953b9c7b5977e07b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985512"
---
# <a name="fmevent_user_refresh-message"></a>\_ \_ Сообщение об обновлении пользователя фмевент

Отправляется в библиотеку DLL расширения, когда пользователь выбирает команду " **Обновить** " из меню " **вид** " в диспетчере файлов. Расширение может использовать это уведомление для обновления меню.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Библиотека DLL расширения должна вернуть нуль, если обрабатывает это сообщение.

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

 

 




