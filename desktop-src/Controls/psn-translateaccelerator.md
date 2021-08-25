---
title: Код уведомления PSN_TRANSLATEACCELERATOR (Пршт. h)
description: Уведомляет вкладку свойств о получении сообщения клавиатуры. Она предоставляет странице возможность сделать закрытый клавиатурный перевод с помощью сочетания клавиш. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR кода уведомления Windows элементы управления
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
ms.openlocfilehash: 7ca25ed7dd2a2fa2b11e0854f7fe9e4bb4afb9aa47ec52c21bc1c6e346ebf16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914494"
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

## <a name="remarks"></a>Remarks

Чтобы задать возвращаемое значение, процедура диалогового окна для страницы должна использовать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) со \_ значением DWL мсгресулт. Процедура диалогового окна должна возвращать **значение true**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

