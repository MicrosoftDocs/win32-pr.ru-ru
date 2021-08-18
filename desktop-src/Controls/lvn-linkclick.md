---
title: Код уведомления LVN_LINKCLICK (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что была нажата ссылка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- LVN_LINKCLICK кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e89db641bc17e8c3d9d548bdf502e077c88dfc6c7452f8059b085c3432d23bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019072"
---
# <a name="lvn_linkclick-notification-code"></a>\_Код уведомления ЛВН линккликк

Сообщает родительскому окну элемента управления "представление списка", что была нажата ссылка. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) . Идентификатор группы, содержащей ссылку, находится в элементе **iSubItem** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

В следующем примере показано, как приложение может реагировать на этот код уведомления в обработчике сообщений [**WM \_ Notify**](wm-notify.md) . В этом примере переключается свернутое состояние группы и устанавливается соответствующий текст ссылки.

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





