---
description: Посылается, когда приложение запрашивает создание окна с помощью вызова функции CreateWindowEx или CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Сообщение WM_CREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ff80c3fe0c12aeaa8b968d2d609fb7d10765c0474ffc001b9b18385e38d149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931284"
---
# <a name="wm_create-message"></a>\_Создание сообщения WM

Посылается, когда приложение запрашивает создание окна с помощью вызова функции [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) или [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . (Сообщение отправляется перед возвратом функции.) Процедура окна нового окна получает это сообщение после создания окна, но до того, как окно становится видимым.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , содержащую сведения о создаваемом окне.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно вернуть ноль, чтобы продолжить создание окна. Если приложение возвращает значение – 1, окно уничтожается, а функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) или [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) возвращает **нулевой** маркер.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM \_ нккреате**](wm-nccreate.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
