---
title: Код уведомления TDN_TIMER (Коммктрл. h)
description: Отправляется диалоговым окном задачи примерно каждые 200 миллисекунд.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654697"
---
# <a name="tdn_timer-notification-code"></a>\_Код уведомления о таймере ТДН

Отправляется диалоговым окном задачи примерно каждые 200 миллисекунд. Этот код уведомления отправляется, если \_ флаг таймера обратного вызова TDF \_ задан в элементе **dwFlags** структуры [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) , переданной в функцию [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода **таскдиалогиндирект** .


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение **типа DWORD** , указывающее количество миллисекунд, прошедших с момента создания диалогового окна или возвращенного этим кодом уведомления **\_ false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Чтобы сбросить значение TickCount, приложение должно вернуть **\_ значение false**. в противном случае значение TickCount продолжит расти.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





