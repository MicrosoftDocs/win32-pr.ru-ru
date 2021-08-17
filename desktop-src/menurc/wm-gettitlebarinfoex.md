---
title: Сообщение WM_GETTITLEBARINFOEX (Winuser. h)
description: Отправлено на запрос расширенных сведений в строке заголовка. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1acbe85afa1871caf796c70a9535f5646d2511317a0e9ee0564db55101a16449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869670"
---
# <a name="wm_gettitlebarinfoex-message"></a>\_Сообщение ЖЕТТИТЛЕБАРИНФОЕКС WM

Отправлено на запрос расширенных сведений в строке заголовка. Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется и должен быть равен 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**титлебаринфоекс**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) . Отправитель сообщения отвечает за выделение памяти для этой структуры. Задайте для элемента **кбсизе** этой структуры значение `sizeof(TITLEBARINFOEX)` перед передачей этой структуры вместе с сообщением.

</dd> </dl>

## <a name="remarks"></a>Remarks

В следующем примере показано, как получатель сообщения приводит значение **lParam** для получения структуры [**титлебаринфоекс**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о меню](menus.md)
</dt> </dl>

 

