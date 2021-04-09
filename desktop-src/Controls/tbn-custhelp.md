---
title: Код уведомления TBN_CUSTHELP (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь выбрал кнопку «Справка» в диалоговом окне Настройка панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- TBN_CUSTHELP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891645"
---
# <a name="tbn_custhelp-notification-code"></a>\_Код уведомления ТБН кусселп

Сообщает родительскому окну панели инструментов, что пользователь выбрал кнопку «Справка» в диалоговом окне Настройка панели инструментов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





