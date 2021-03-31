---
title: Сообщение MCM_GETCURSEL (Коммктрл. h)
description: Извлекает текущую выбранную дату. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- Элементы управления Windows для MCM_GETCURSEL сообщений
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491448"
---
# <a name="mcm_getcursel-message"></a>MCM \_ сообщение

Извлекает текущую выбранную дату. Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , которая будет принимать текущую выбранную информацию о дате. Этот параметр должен быть допустимым адресом и не может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае. Это сообщение всегда будет завершаться ошибкой при применении к элементам управления "Календарь на месяц", для которых задан стиль "Многоэлементный [**\_ Выбор MCS**](month-calendar-control-styles.md) ".

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

 

