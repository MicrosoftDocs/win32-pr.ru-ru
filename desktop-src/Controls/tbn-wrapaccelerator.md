---
title: Код уведомления TBN_WRAPACCELERATOR (Коммктрл. h)
description: Запрашивает индекс кнопки на одной или нескольких панелях инструментов, соответствующих указанному символу ускорителя. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c5ec222f387108e2cb4d240e6dddf0fcb904d814097a96624a177425eb805ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105034"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>\_Код уведомления ТБН врапакцелератор

Запрашивает индекс кнопки на одной или нескольких панелях инструментов, соответствующих указанному символу ускорителя. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру, содержащую символ клавиши быстрого вызова и получающий индекс соответствующей кнопки. Индекс имеет значение-1, если ускоритель не соответствует команде.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Значение true** , если возвращается индекс; в противном случае — **значение false**.

## <a name="remarks"></a>Remarks

Приложения с одной или несколькими панелями инструментов могут получить этот код уведомления.

Структура **нмтбврапакцелератор** должна быть определена приложением следующим образом:

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





