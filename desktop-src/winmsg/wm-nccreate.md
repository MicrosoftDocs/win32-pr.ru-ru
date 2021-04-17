---
description: Отправляется перед \_ сообщением о создании WM при первом создании окна.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Сообщение WM_NCCREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711949"
---
# <a name="wm_nccreate-message"></a>\_Сообщение НККРЕАТЕ WM

Отправляется перед сообщением о [**\_ создании WM**](wm-create.md) при первом создании окна.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , содержащую сведения о создаваемом окне. Элементы **CREATESTRUCT** идентичны параметрам функции [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно возвращать **значение true** , чтобы продолжить создание окна. Если приложение возвращает **значение false**, функция [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) вернет **нулевой** маркер.

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

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**\_Создание WM**](wm-create.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
