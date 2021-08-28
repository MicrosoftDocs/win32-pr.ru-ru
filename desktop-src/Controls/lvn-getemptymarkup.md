---
title: Код уведомления LVN_GETEMPTYMARKUP (Коммктрл. h)
description: Посылается элементом управления List-View родительскому окну, если элемент управления не имеет элементов. \_Код уведомления ЛВН жетемптимаркуп — это запрос родительского окна для предоставления текста разметки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5da87d0585a22d41743e58e946c4b1b39ca24c8bb131e9084596ce4f8c2b7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005705"
---
# <a name="lvn_getemptymarkup-notification-code"></a>\_Код уведомления ЛВН жетемптимаркуп

Посылается элементом управления List-View родительскому окну, если элемент управления не имеет элементов. \_Код уведомления ЛВН жетемптимаркуп — это запрос родительского окна для предоставления текста разметки. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлвемптимаркуп**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Задайте элементы этой структуры, чтобы предоставить текст разметки для элемента управления "представление списка".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , чтобы задать текст разметки в элементе управления "список", или **false** в противном случае.

## <a name="remarks"></a>Remarks

Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвемптимаркуп**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Параметр *wParam* содержит идентификатор элемента управления, который отправляет это сообщение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





