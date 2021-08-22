---
title: Код уведомления HDN_DROPDOWN (Коммктрл. h)
description: Посылается элементом управления "заголовок" родительскому элементу при щелчке стрелки раскрывающегося списка в элементе управления "заголовок". Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN кода уведомления Windows элементы управления
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
ms.openlocfilehash: 8a5a7e423c40fa655a9eca0e5b97c20a2d61add1e6c0b7f66b65a69afdc32a55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435574"
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

## <a name="remarks"></a>Remarks

Пример в разделе синтаксиса показывает, как получатель уведомлений применяет **lParam** для получения структуры [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** содержит идентификатор элемента управления, который отправляет это сообщение.

Это сообщение отправляется, только если \_ для элемента заголовка задан стиль ХДФ SPLITBUTTON.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





