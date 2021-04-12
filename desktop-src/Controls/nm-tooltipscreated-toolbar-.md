---
title: Код уведомления NM_TOOLTIPSCREATED (Toolbar) (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что панель инструментов создала элемент управления ToolTip. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- Элементы управления Windows для кода уведомления NM_TOOLTIPSCREATED (панель инструментов)
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489954"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a>\_Код уведомления "NM тултипскреатед (панель инструментов)"

Сообщает родительскому окну панели инструментов, что панель инструментов создала элемент управления ToolTip. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтултипскреатед**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Элемент управления ToolBar игнорирует возвращаемое значение из этого кода уведомления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





