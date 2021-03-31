---
title: Сообщение WM_CAPTURECHANGED (Winuser. h)
description: Отправляется в окно, которое теряет захват мыши.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- WM_CAPTURECHANGED ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135639"
---
# <a name="wm_capturechanged-message"></a>\_Сообщение КАПТУРЕЧАНЖЕД WM

Отправляется в окно, которое теряет захват мыши.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на окно, получив захват мыши.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Комментарии

Окно получает это сообщение, даже если оно вызывает [**релеасекаптуре**](/windows/win32/api/winuser/nf-winuser-releasecapture) . Приложение не должно пытаться установить захват мыши в ответ на это сообщение.

При получении этого сообщения окно должно перерисовывать себя при необходимости, чтобы отразить новое состояние захвата мыши.

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

[**релеасекаптуре**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[**сеткаптуре**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ввод с помощью мыши](mouse-input.md)
</dt> </dl>

 

