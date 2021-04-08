---
title: Код уведомления HDN_OVERFLOWCLICK (Коммктрл. h)
description: Посылается элементом управления "заголовок" родительскому элементу при нажатии кнопки переполнения заголовка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892022"
---
# <a name="hdn_overflowclick-notification-code"></a>\_Код уведомления ХДН оверфловкликк

Посылается элементом управления "заголовок" родительскому элементу при нажатии кнопки переполнения заголовка. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* \[ окне\]
</dt> <dd>

Указатель на структуру [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) , описывающую код уведомления. Вызывающий процесс отвечает за выделение этой структуры, включая вложенную структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) . Задайте элементы структуры **NMHDR** , включая элемент *кода* , который должен иметь значение ХДН \_ оверфловкликк.

Задайте для элемента **Член iItem** структуры [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) индекс первого элемента заголовка, который не является видимым, и, таким же, должен быть отображен при переполнении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Получатель уведомлений выполняет приведение **lParam** для получения структуры [**нмхеадер**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** содержит идентификатор элемента управления, который отправляет уведомление.

Это сообщение отправляется, только если для элемента управления "заголовок" задано [**\_ переполнение Style HDS**](header-control-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





