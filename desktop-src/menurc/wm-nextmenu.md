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
ms.openlocfilehash: 635ce19efbcfdfd8451f929affbbe0fe2b2c000bc4912977062f3fba2c54e9c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952084"
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

## <a name="remarks"></a>Remarks

В ответ на это сообщение приложение может указать меню для перехода в **хменунекст** член [**мдинекстмену**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) и окно для получения сообщений уведомления меню в элементе **хвнднекст** структуры **мдинекстмену** . Необходимо задать оба элемента, чтобы изменения вступили в силу (они изначально равны **null**).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**мдинекстмену**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Зрения**
</dt> <dt>

[Меню](menus.md)
</dt> </dl>

 

