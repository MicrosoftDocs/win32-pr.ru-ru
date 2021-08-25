---
title: Код уведомления TBN_RESET (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь выполнил Сброс содержимого диалогового окна "Настройка панели инструментов". Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET кода уведомления Windows элементы управления
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
ms.openlocfilehash: b7852ee64dcf741dd291965e86d3d73f6113c1c8270bfa948d8d547fa99b9c01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876624"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





