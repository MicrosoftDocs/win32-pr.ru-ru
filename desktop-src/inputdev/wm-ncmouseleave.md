---
title: Сообщение WM_NCMOUSELEAVE (Winuser. h)
description: Передается в окно, когда курсор покидает неклиентскую область окна, указанную в предыдущем вызове метода TrackMouseEven.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- WM_NCMOUSELEAVE ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691800"
---
# <a name="wm_ncmouseleave-message"></a>\_Сообщение НКМАУСЕЛЕАВЕ WM

Передается в окно, когда курсор покидает неклиентскую область окна, указанную в предыдущем вызове метода [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCMOUSELEAVE                 0x02A2
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

## <a name="remarks"></a>Комментарии

При создании этого сообщения все записи, запрошенные [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) , отменяются. Приложение должно вызвать **TrackMouseEven** , когда указатель мыши перейдет в окно, если он требует дополнительного отслеживания поведения при наведении указателя мыши.

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

[**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVEN**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ MOUSELEAVE**](wm-mouseleave.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ввод с помощью мыши](mouse-input.md)
</dt> </dl>

 

