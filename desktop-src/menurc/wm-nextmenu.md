---
title: Сообщение WM_NEXTMENU (Winuser. h)
description: Отправляется в приложение, когда для переключения между строкой меню и системным меню используется клавиша со стрелкой вправо или влево.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989405"
---
# <a name="wm_nextmenu-message"></a>\_Сообщение НЕКСТМЕНУ WM

Отправляется в приложение, когда для переключения между строкой меню и системным меню используется клавиша со стрелкой вправо или влево.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Код виртуального ключа для ключа. См. раздел [**коды виртуальных клавиш**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**мдинекстмену**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) , содержащую сведения о меню, которое должно быть активировано.

</dd> </dl>

## <a name="remarks"></a>Комментарии

В ответ на это сообщение приложение может указать меню для перехода в **хменунекст** член [**мдинекстмену**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) и окно для получения сообщений уведомления меню в элементе **хвнднекст** структуры **мдинекстмену** . Необходимо задать оба элемента, чтобы изменения вступили в силу (они изначально равны **null**).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**мдинекстмену**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Зрения**
</dt> <dt>

[Меню](menus.md)
</dt> </dl>

 

