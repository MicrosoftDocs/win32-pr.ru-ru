---
title: Сообщение MCM_GETTODAY (Коммктрл. h)
description: Извлекает сведения о дате для даты, указанной как \ 0034; сегодня \ 0034; для элемента управления "месячный календарь". Это сообщение можно отправить явно или с помощью \_ макроса монскал ontoday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- элементы управления Windows сообщений MCM_GETTODAY
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6925ff24a2d3e042a4f2c752d87642f74345116fc5cc7f94e00e811d453be4fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019032"
---
# <a name="mcm_gettoday-message"></a>\_Сообщение MCM

Извлекает сведения о дате для даты, указанной в поле "сегодня", для элемента управления "месячный календарь". Это сообщение можно отправить явно или с помощью макроса [**монскал \_ ontoday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , которая получит сведения о дате. Этот параметр должен быть допустимым адресом и не может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Время в элементе управления ' календарь на месяц '](month-calendar-controls.md)
</dt> </dl>

 

