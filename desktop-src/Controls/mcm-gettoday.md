---
title: Сообщение MCM_GETTODAY (Коммктрл. h)
description: Извлекает сведения о дате для даты, указанной как \ 0034; сегодня \ 0034; для элемента управления "месячный календарь". Это сообщение можно отправить явно или с помощью \_ макроса монскал ontoday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- Элементы управления Windows для MCM_GETTODAY сообщений
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
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988726"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Время в элементе управления ' календарь на месяц '](month-calendar-controls.md)
</dt> </dl>

 

