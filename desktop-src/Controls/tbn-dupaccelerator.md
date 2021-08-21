---
title: Код уведомления TBN_DUPACCELERATOR (Коммктрл. h)
description: Определяет, можно ли использовать сочетание клавиш на двух или более активных панелях инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ff0059a6071db79cab91fcf903a1e68f3550c766b3d16cd3571c3a785e7368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829337"
---
# <a name="tbn_dupaccelerator-notification-code"></a>\_Код уведомления ТБН дупакцелератор

Определяет, можно ли использовать сочетание клавиш на двух или более активных панелях инструментов. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру, которая предоставляет ускоритель и получает значение, указывающее, реагируют ли несколько панелей инструментов на один и тот же символ.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха, в противном случае — **значение false**.

## <a name="remarks"></a>Remarks

Приложение должно объявить структуру **нмтбдупакцелератор** следующим образом:

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





