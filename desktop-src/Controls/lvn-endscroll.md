---
title: Сообщение LVN_ENDSCROLL (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", когда заканчивается операция прокрутки. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- Элементы управления Windows для LVN_ENDSCROLL сообщений
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892830"
---
# <a name="lvn_endscroll-message"></a>\_Сообщение ЛВН ендскролл

Сообщает родительскому окну элемента управления "представление списка", когда заканчивается операция прокрутки. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлвскролл**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) , содержащую горизонтальную или вертикальную позицию, где заканчивается операция прокрутки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





