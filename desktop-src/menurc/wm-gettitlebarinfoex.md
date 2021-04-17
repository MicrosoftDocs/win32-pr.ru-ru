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
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415013"
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

## <a name="remarks"></a>Комментарии

В следующем примере показано, как получатель сообщения приводит значение **lParam** для получения структуры [**титлебаринфоекс**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о меню](menus.md)
</dt> </dl>

 

