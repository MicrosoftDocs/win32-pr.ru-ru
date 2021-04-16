---
title: Сообщение WM_POINTERCAPTURECHANGED
description: Отправляется в окно, которое теряет захват входного указателя.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- WM_POINTERCAPTURECHANGED сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719211"
---
# <a name="wm_pointercapturechanged-message"></a>Сообщение WM_POINTERCAPTURECHANGED

Отправляется в окно, которое теряет захват входного указателя.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Содержит сведения о потере входного указателя. Чтобы получить идентификатор указателя, используйте [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) .

</dd> <dt>

*lParam* 
</dt> <dd>

Содержит маркер окна, записывающего указатель ввода. Это значение может быть равно NULL, если это окно больше не захвачено указателем.

Если это сообщение создается на основе внутренней обработки, то значением может быть маркер окна, получающего сообщение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Комментарии

Окно должно использовать это уведомление для прекращения обработки последующих сообщений и инициации очистки, необходимой для потери указателя. Обработка жестов, связанных с указателем, должна также завершаться (например, путем вызова [**стопинтерактионконтекст**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)), а оставшиеся контакты повторно связаны с окном.

Как правило, если окно получает уведомление **WM_POINTERCAPTURECHANGED** , то последующие уведомления, связанные с указателем ввода, не принимаются. По этой причине не следует зависеть от парных уведомлений, таких как [**WM_POINTERENTER**](wm-pointerenter.md) и [**WM_POINTERLEAVE**](wm-pointerleave.md).

**WM_POINTERCAPTURECHANGED** не содержит [**POINTER_INFO**](/previous-versions/windows/desktop/api) данных. В отличие от установленного флага [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) , данные, возвращаемые [**жетпоинтеринфо**](/previous-versions/windows/desktop/api) (или любым вариантом), идентичны тому, что были возвращены перед уведомлением.

Если приложение не обрабатывает это уведомление, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) может создать одно или несколько [**WM_GESTURE**](../wintouch/wm-gesture.md) сообщений или, если жест не распознается, **дефвиндовпрок** может создавать ввод с помощью мыши.

Если приложение выборочно потребляет некоторые входные данные указателя и передает оставшуюся часть в [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca), то результирующее поведение не определено.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения](messages.md)
</dt> </dl>

 

