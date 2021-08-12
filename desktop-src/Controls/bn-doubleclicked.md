---
title: Код уведомления BN_DOUBLECLICKED (Winuser. h)
description: BN_DOUBLECLICKED код уведомления — отправляется, когда пользователь дважды нажимает кнопку.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce43cebee93516f929f9a763c14dd51d9d486470eeb93818b9605c3f23a1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674128"
---
# <a name="bn_doubleclicked-notification-code"></a>\_Код уведомления млрд долл даублекликкед

Посылается, когда пользователь дважды нажимает кнопку. Этот код уведомления отправляется автоматически для кнопок [**BS \_ усербуттон**](button-styles.md), [**BS \_**](button-styles.md)и [**BS \_ овнердрав**](button-styles.md) . Другие типы кнопок отправляют млрд долл \_ даублекликкед только в том случае, если они имеют стиль " [**BS \_**](button-styles.md) ".

Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер кнопки.

</dd> </dl>

## <a name="remarks"></a>Remarks

МЛРД долл \_ даублекликкед совпадает с кодом уведомления [млрд долл \_ дблклк](bn-dblclk.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



 

