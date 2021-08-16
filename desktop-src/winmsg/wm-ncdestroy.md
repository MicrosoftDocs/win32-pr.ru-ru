---
description: Уведомляет окно о том, что удаляется неклиентская область. Функция Дестройвиндов отправляет \_ сообщение WM нкдестрой в окно после \_ сообщения WM destroy.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Сообщение WM_NCDESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2e74db0abf22fc2fb3d2a16b5cc63187514d1bee26079490c8d19eae13787e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200050"
---
# <a name="wm_ncdestroy-message"></a>\_Сообщение НКДЕСТРОЙ WM

Уведомляет окно о том, что удаляется неклиентская область. Функция [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) отправляет сообщение **WM \_ нкдестрой** в окно после сообщения [**WM \_ destroy**](wm-destroy.md) .[**WM \_ destroy**](wm-destroy.md) используется для высвобождения выделенного объекта памяти, связанного с окном.

Сообщение **WM \_ нкдестрой** отправляется после уничтожения дочерних окон. Напротив, [**WM \_ destroy**](wm-destroy.md) отправляется перед уничтожением дочерних окон.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Remarks

Это сообщение освобождает память, выделенную для окна.

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

[**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**WM \_ destroy**](wm-destroy.md)
</dt> <dt>

[**WM \_ нккреате**](wm-nccreate.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
