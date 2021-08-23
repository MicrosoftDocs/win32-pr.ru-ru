---
title: Код уведомления TBN_WRAPHOTITEM (Коммктрл. h)
description: Уведомляет приложение с двумя или более панелями инструментов, которые должны быть изменены в активном элементе. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM кода уведомления Windows элементы управления
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
ms.openlocfilehash: 33c6bd1f2e750a2fd71dc053d31ca452fa581891037db73d356e5405476b28de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293368"
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

## <a name="remarks"></a>Remarks

Структура **нмтбврафотитем** должна быть определена приложением следующим образом:

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





