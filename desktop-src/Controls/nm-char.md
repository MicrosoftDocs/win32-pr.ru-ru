---
title: Код уведомления NM_CHAR (Коммктрл. h)
description: '\_Код уведомления NM char отправляется элементом управления при обработке клавиши знака. Этот код уведомления отправляется в виде \_ сообщения WM notify.'
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR кода уведомления Windows элементы управления
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
ms.openlocfilehash: 73c35871410244bfb69f67c7e0b2c960d0dd50d432ad9cdcfd8765c7df449bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018952"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[NM \_ char (панель инструментов)](nm-char-toolbar.md)
</dt> </dl>

 

 





