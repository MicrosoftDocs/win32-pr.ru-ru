---
title: Код уведомления TRBN_THUMBPOSCHANGING (Коммктрл. h)
description: Уведомляет об изменении расположения бегунка на TrackBar. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f05f67eb20c78f764957e73d2293d32e88f25a73d44d6b58f9a1c310b8d9d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751044"
---
# <a name="trbn_thumbposchanging-notification-code"></a>\_Код уведомления трбн сумбпосчангинг

Уведомляет об изменении расположения бегунка на TrackBar. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтрбсумбпосчангинг**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) . Вызывающий объект отвечает за выделение этой структуры и задание ее членов, включая элементы содержащейся в ней структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы предотвратить перемещение бегунка в указанную точку.

## <a name="remarks"></a>Remarks

Отправьте это уведомление клиентам, которые не прослушивают сообщения [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





