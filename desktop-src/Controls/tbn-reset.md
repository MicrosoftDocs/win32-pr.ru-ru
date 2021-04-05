---
title: Код уведомления TBN_RESET (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь выполнил Сброс содержимого диалогового окна "Настройка панели инструментов". Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071965"
---
# <a name="tbn_reset-notification-code"></a>\_Код уведомления о сбросе ТБН

Сообщает родительскому окну панели инструментов, что пользователь выполнил Сброс содержимого диалогового окна "Настройка панели инструментов". Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвратите ТБНРФ \_ ендкустомизе, чтобы закрыть диалоговое окно Настройка панели инструментов. Все остальные возвращаемые значения игнорируются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





