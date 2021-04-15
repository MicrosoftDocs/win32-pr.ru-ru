---
title: Код уведомления NM_CHAR (Коммктрл. h)
description: '\_Код уведомления NM char отправляется элементом управления при обработке клавиши знака. Этот код уведомления отправляется в виде \_ сообщения WM notify.'
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654726"
---
# <a name="nm_char-notification-code"></a>\_Код уведомления "NM char"

\_Код уведомления NM char отправляется элементом управления при обработке клавиши знака. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмчар**](/windows/win32/api/commctrl/ns-commctrl-nmchar) , которая содержит дополнительные сведения о символе, вызвавшем код уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется большинством элементов управления. Дополнительные сведения см. в документации по отдельным элементам управления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[NM \_ char (панель инструментов)](nm-char-toolbar.md)
</dt> </dl>

 

 





