---
title: Сообщение WM_DRAWCLIPBOARD (Winuser. h)
description: Отправляется в первое окно в цепочке окна просмотра буфера обмена при изменении содержимого буфера обмена. Это позволяет окну просмотра буфера обмена отображать новое содержимое буфера обмена. Окно получает это сообщение через функцию WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- Обмен данными с сообщениями WM_DRAWCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661899"
---
# <a name="wm_drawclipboard-message"></a>\_Сообщение ДРАВКЛИПБОАРД WM

Отправляется в первое окно в цепочке окна просмотра буфера обмена при изменении содержимого буфера обмена. Это позволяет окну просмотра буфера обмена отображать новое содержимое буфера обмена.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DRAWCLIPBOARD                0x0308
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

## <a name="remarks"></a>Комментарии

Это сообщение получит только окно просмотра буфера обмена. Это окна, добавленные в цепочку средства просмотра буфера обмена с помощью функции [**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Каждое окно, получающее **сообщение \_ дравклипбоард WM** , должно вызывать функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) для передачи сообщения в следующее окно в цепочке окна просмотра буфера обмена. Маркер для следующего окна в цепочке возвращается [**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)и может измениться в ответ на сообщение [**\_ чанжекбчаин WM**](wm-changecbchain.md) .

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ чанжекбчаин**](wm-changecbchain.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Буфер обмена](clipboard.md)
</dt> </dl>

 

