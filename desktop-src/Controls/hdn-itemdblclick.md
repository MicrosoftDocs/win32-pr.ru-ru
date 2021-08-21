---
title: Код уведомления HDN_ITEMDBLCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления заголовка, что пользователь дважды щелкнул элемент управления. Этот код уведомления отправляется в виде \_ сообщения WM notify. Только элементы управления "заголовок", для которых задан \_ стиль кнопки HDS, отправляют этот код уведомления.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7117ceb8d17447eed8003f7da3dab70a17252c750bfb3885cd3f235a70b7bb53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544619"
---
# <a name="hdn_itemdblclick-notification-code"></a>\_Код уведомления ХДН итемдблкликк

Сообщает родительскому окну элемента управления заголовка, что пользователь дважды щелкнул элемент управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) . Только элементы управления "заголовок", для которых задан стиль [**\_ кнопки HDS**](header-control-styles.md) , отправляют этот код уведомления.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения об этом коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ХДН \_ ИТЕМДБЛКЛИККВ** (Юникод) и **ХДН \_ итемдблкликка** (ANSI)<br/>         |



 

 





