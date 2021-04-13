---
title: Код уведомления TBN_WRAPHOTITEM (Коммктрл. h)
description: Уведомляет приложение с двумя или более панелями инструментов, которые должны быть изменены в активном элементе. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490191"
---
# <a name="tbn_wraphotitem-notification-code"></a>\_Код уведомления ТБН врафотитем

Уведомляет приложение с двумя или более панелями инструментов, которые должны быть изменены в активном элементе. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру, которая содержит старый элемент Hot (**истарт**) и указывает, находится ли новый горячий элемент перед ним (**идир** =-1) или после него (**идир** = 1), а также по причине изменения горячего элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Значение true** , если приложение обрабатывает горячее изменение элемента; в противном случае — **false**.

## <a name="remarks"></a>Комментарии

Структура **нмтбврафотитем** должна быть определена приложением следующим образом:

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





