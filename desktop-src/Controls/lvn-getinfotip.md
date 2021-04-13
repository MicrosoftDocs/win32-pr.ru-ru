---
title: Код уведомления LVN_GETINFOTIP (Коммктрл. h)
description: Отправляется элементом управления "представление списка" с большим значком, имеющим \_ \_ Расширенный стиль подсказки LVS ex.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535645"
---
# <a name="lvn_getinfotip-notification-code"></a>\_Код уведомления ЛВН жетинфотип

Отправляется элементом управления "представление списка" с большим значком, имеющим расширенный стиль [**\_ \_ подсказки LVS ex**](extended-list-view-styles.md) . Этот код уведомления отправляется, когда элемент управления "представление списка" запрашивает дополнительную текстовую информацию для отображения в подсказке. Он отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлвжетинфотип**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) , содержащую сведения об этом коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого уведомления не используется.

## <a name="remarks"></a>Комментарии

Этот код уведомления отправляется только элементами управления "представление списка", у которых есть расширенный стиль [**\_ \_ подсказки LVS ex**](extended-list-view-styles.md) . \_Код уведомления ЛВН жетинфотип отправляется только для подэлемента 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ЛВН \_ ЖЕТИНФОТИПВ** (Юникод) и **ЛВН \_ жетинфотипа** (ANSI)<br/>             |



 

 





