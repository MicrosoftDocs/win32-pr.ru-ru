---
title: Код уведомления NM_RELEASEDCAPTURE (Главная панель) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления главной панели, что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 1196260f-b9ba-4a9e-80a7-e126196c3beb
keywords:
- элементы управления Windows кода уведомления NM_RELEASEDCAPTURE (главная панель)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0601a8daa581b9f3dea477c849d668e222308bdcb991fe4c107470c341ff5661
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018782"
---
# <a name="nm_releasedcapture-rebar-notification-code"></a>\_Код уведомления "NM релеаседкаптуре" (Главная панель)

Сообщает родительскому окну элемента управления главной панели, что элемент управления освобождает захват мыши. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую дополнительные сведения об этом уведомлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Элемент управления игнорирует возвращаемое значение из этого кода уведомления.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





