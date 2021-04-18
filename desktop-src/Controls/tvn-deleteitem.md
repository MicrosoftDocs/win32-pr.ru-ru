---
title: Код уведомления TVN_DELETEITEM (Коммктрл. h)
description: Сообщает родительскому окну элемента управления древовидного представления о том, что элемент удаляется. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2953ca0cf272b102a08fba0516d4891dccde9daf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490839"
---
# <a name="tvn_deleteitem-notification-code"></a>\_Код уведомления ТВН DELETEITEM

Сообщает родительскому окну элемента управления древовидного представления о том, что элемент удаляется. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтривиев**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Элемент **итемолд** — это структура [**Твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , элементы **хитем** и **lParam** которой содержат действительные сведения об удаляемом элементе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Комментарии

Если член **lParam** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) указывает на память, выделенную приложением, вы можете освободить его при получении \_ кода уведомления ТВН DELETEITEM.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ ДЕЛЕТЕИТЕМВ** (Юникод) и **ТВН \_ делетеитема** (ANSI)<br/>             |



 

 





