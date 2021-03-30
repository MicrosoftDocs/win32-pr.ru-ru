---
title: Сообщение WM_CHANGECBCHAIN (Winuser. h)
description: Отправляется в первое окно в цепочке окна просмотра буфера обмена при удалении окна из цепочки. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- Обмен данными с сообщениями WM_CHANGECBCHAIN
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136171"
---
# <a name="wm_changecbchain-message"></a>\_Сообщение ЧАНЖЕКБЧАИН WM

Отправляется в первое окно в цепочке окна просмотра буфера обмена при удалении окна из цепочки.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер окна, удаляемого из цепочки средства просмотра буфера обмена.

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер следующего окна в цепочке после удаляемого окна. Этот параметр имеет **значение NULL** , если удаляемое окно является последним окном в цепочке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

Каждое окно просмотра буфера обмена сохраняет маркер в следующем окне в цепочке окна просмотра буфера обмена. Изначально этот маркер является возвращаемым значением функции [**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Когда окно просмотра буфера обмена получает сообщение **WM \_ чанжекбчаин** , оно должно вызывать функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) для передачи сообщения следующему окну в цепочке, если только следующее окно не является удаляемым окном. В этом случае средство просмотра буфера обмена должно сохранить маркер, заданный параметром *lParam* , в качестве следующего окна в цепочке.

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

**Зрения**
</dt> <dt>

[Буфер обмена](clipboard.md)
</dt> </dl>

 

