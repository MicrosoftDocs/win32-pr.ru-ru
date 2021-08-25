---
title: Код уведомления RBN_AUTOSIZE (Коммктрл. h)
description: Посылается элементом управления главной панели, созданным с помощью стиля автомасштабирования RBS, \_ когда Главная панель автоматически изменяет размер. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32c0ef601562c6887e05c78c06a66cf61e330843769eb3bb66105eb941e09339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985374"
---
# <a name="rbn_autosize-notification-code"></a>\_Код уведомления РБН AUTOSIZE

Посылается элементом управления главной панели, созданным с помощью стиля автомасштабирования [**RBS \_**](rebar-control-styles.md) , когда Главная панель автоматически изменяет размер. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмрбаутосизе**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) , содержащую сведения об операции изменения размера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого уведомления не используется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





