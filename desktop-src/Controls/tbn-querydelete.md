---
title: Код уведомления TBN_QUERYDELETE (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, можно ли удалить кнопку с панели инструментов, пока пользователь настраивает панель инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a01d1322ce8461c5cdb53fc76cfc220bbb5d292dedbe589d8b6ada5a48756d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077888"
---
# <a name="tbn_querydelete-notification-code"></a>\_Код уведомления ТБН куериделете

Сообщает родительскому окну панели инструментов, можно ли удалить кнопку с панели инструментов, пока пользователь настраивает панель инструментов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Член **iItem** содержит отсчитываемый от нуля индекс удаляемой кнопки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы разрешить удаление кнопки, или **значение false** , чтобы предотвратить удаление кнопки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





