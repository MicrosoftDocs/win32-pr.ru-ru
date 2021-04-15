---
title: Код уведомления PSN_TRANSLATEACCELERATOR (Пршт. h)
description: Уведомляет вкладку свойств о получении сообщения клавиатуры. Она предоставляет странице возможность сделать закрытый клавиатурный перевод с помощью сочетания клавиш. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654423"
---
# <a name="psn_translateaccelerator-notification-code"></a>\_Код уведомления PSN TRANSLATEACCELERATOR

Уведомляет вкладку свойств о получении сообщения клавиатуры. Она предоставляет странице возможность сделать закрытый клавиатурный перевод с помощью сочетания клавиш. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления. Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** структуры **NMHDR** содержит маркер для страницы свойств. Член **lParam** структуры **пшнотифи** — это указатель [**на сообщение сообщения.**](/windows/win32/api/winuser/ns-winuser-msg) Его можно привести к типу **лпмсг** , чтобы получить доступ к параметрам сообщения, которое необходимо перевести.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ПСНРЕТ \_ мессажехандлед, чтобы указать, что дальнейшая обработка не требуется. Возвращает ПСНРЕТ \_ , чтобы запросить нормальную обработку.

## <a name="remarks"></a>Комментарии

Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна использовать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) со \_ значением DWL мсгресулт. Процедура диалогового окна должна возвращать **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

