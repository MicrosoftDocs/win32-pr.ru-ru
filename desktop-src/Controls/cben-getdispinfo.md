---
title: Код уведомления CBEN_GETDISPINFO (Коммктрл. h)
description: Отправлено, чтобы получить отображаемые сведения о элементе обратного вызова. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896d282426c11f40fe949c73f44eb963a399c5c210e839198527f9bc903e2fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413697"
---
# <a name="cben_getdispinfo-notification-code"></a>\_Код уведомления кбен жетдиспинфо

Отправлено, чтобы получить отображаемые сведения о элементе обратного вызова. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмкомбобоксекс**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) , содержащую сведения о коде уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.

## <a name="remarks"></a>Remarks

Структура [**нмкомбобоксекс**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) содержит структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) . Элемент **Mask** задает сведения, запрашиваемые элементом управления.

Заполните соответствующие члены структуры, чтобы вернуть запрошенные сведения в элемент управления. Если обработчик сообщений устанавливает для элемента **маски** структуры [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) значение кбеиф \_ di \_ сетитем, элемент управления сохраняет информацию и не запрашивает их снова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Кбен \_ ЖЕТДИСПИНФОВ** (Юникод) и **кбен \_ жетдиспинфоа** (ANSI)<br/>         |



 

 





