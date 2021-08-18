---
title: Сообщение WM_RENDERALLFORMATS (Winuser. h)
description: Отправляется владельцу буфера обмена до его уничтожения, если владелец буфера обмена откладывает отложенную отрисовку одного или нескольких форматов буфера обмена.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77dae9b44cb379ed62c99c601d308fdec500440a9ebad0ffeaffad16ec780dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636064"
---
# <a name="wm_renderallformats-message"></a>\_Сообщение РЕНДЕРАЛЛФОРМАТС WM

Отправляется владельцу буфера обмена до его уничтожения, если владелец буфера обмена откладывает отложенную отрисовку одного или нескольких форматов буфера обмена. Чтобы содержимое буфера обмена оставалось доступным для других приложений, владелец буфера обмена должен визуализировать данные во всех форматах, которые он способен создать, и поместить данные в буфер обмена, вызвав функцию [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется и должен быть равен нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется и должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

При ответе на **сообщение WM \_ рендераллформатс** приложение должно вызвать функцию [**опенклипбоард**](/windows/win32/api/winuser/nf-winuser-openclipboard) , а затем проверить, что он по-прежнему является владельцем буфера обмена, вызвав функцию [**жетклипбоардовнер**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) перед вызовом [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).

Приложение должно проверить, что он по-прежнему является владельцем буфера обмена после открытия буфера обмена, так как после того, как он получит сообщение **WM \_ рендераллформатс** , но до того, как он откроет буфер обмена, другое приложение могло открыться и стать владельцем буфера обмена, и данные этого приложения не должны перезаписываться.

В большинстве случаев приложение не должно вызывать функцию [**емптиклипбоард**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) перед вызовом [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), так как это приведет к удалению форматов буфера обмена, которые приложение уже отрисовывает.

При возвращении приложения система удаляет все неотображенные форматы из списка доступных форматов буфера обмена. Дополнительные сведения о отложенной отрисовке см. в разделе [отложенная визуализация](clipboard-operations.md#delayed-rendering).

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

[**емптиклипбоард**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**опенклипбоард**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERFORMAT**](wm-renderformat.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Буфер обмена](clipboard.md)
</dt> </dl>

 

