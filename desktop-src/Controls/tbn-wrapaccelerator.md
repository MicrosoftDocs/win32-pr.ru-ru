---
title: Код уведомления TBN_WRAPACCELERATOR (Коммктрл. h)
description: Запрашивает индекс кнопки на одной или нескольких панелях инструментов, соответствующих указанному символу ускорителя. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR кода уведомления элементы управления Windows
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
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654440"
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

## <a name="remarks"></a>Комментарии

Приложения с одной или несколькими панелями инструментов могут получить этот код уведомления.

Структура **нмтбврапакцелератор** должна быть определена приложением следующим образом:

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





