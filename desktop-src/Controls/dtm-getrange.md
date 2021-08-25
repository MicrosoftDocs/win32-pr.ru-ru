---
title: Сообщение DTM_GETRANGE (Коммктрл. h)
description: Возвращает текущее минимальное и максимальное допустимое системное время для элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать макрос DateTime \_ .
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- элементы управления Windows сообщений DTM_GETRANGE
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9c0c90780e4bcd35da2d410f7b4743547cbd8d31ac06293c411f2415e4e408
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877954"
---
# <a name="dtm_getrange-message"></a>Сообщение DTMного \_ диапазона

Возвращает текущее минимальное и максимальное допустимое системное время для элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать макрос [**DateTime \_**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив структур [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) с двумя элементами.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , которое представляет собой сочетание гдтр \_ min или гдтр \_ Max. Первый элемент массива [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) содержит минимальное допустимое время, если \_ задано значение гдтр min. Второй элемент массива **SYSTEMTIME** содержит максимально допустимое время, если \_ задано значение гдтр Max.

## <a name="remarks"></a>Remarks

Средство выбора даты и времени отображает только даты и время, которые находятся в пределах указанного диапазона, запрещая пользователю выбирать дату и время, находящиеся за пределами диапазона. Если сообщение [**DTM \_ сетсистемтиме**](dtm-setsystemtime.md) указывает дату и время, которые выходят за пределы диапазона, произойдет сбой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

