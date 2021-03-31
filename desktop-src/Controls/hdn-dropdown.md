---
title: Код уведомления HDN_DROPDOWN (Коммктрл. h)
description: Посылается элементом управления "заголовок" родительскому элементу при щелчке стрелки раскрывающегося списка в элементе управления "заголовок". Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892841"
---
# <a name="hdn_dropdown-notification-code"></a>\_Код уведомления раскрывающегося списка ХДН

Посылается элементом управления "заголовок" родительскому элементу при щелчке стрелки раскрывающегося списка в элементе управления "заголовок". Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , содержащую сведения о элементе управления "заголовок".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Пример в разделе синтаксиса показывает, как получатель уведомлений применяет **lParam** для получения структуры [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** содержит идентификатор элемента управления, который отправляет это сообщение.

Это сообщение отправляется, только если \_ для элемента заголовка задан стиль ХДФ SPLITBUTTON.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





