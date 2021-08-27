---
title: Код уведомления TDN_TIMER (Коммктрл. h)
description: Отправляется диалоговым окном задачи примерно каждые 200 миллисекунд.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER кода уведомления Windows элементы управления
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
ms.openlocfilehash: eaf3f5d72ef8267c6600decf070875b2dd109114f910d09a5ca343f8fde44005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104454"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





