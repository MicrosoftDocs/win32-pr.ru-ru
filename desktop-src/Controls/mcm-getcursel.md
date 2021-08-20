---
title: Сообщение MCM_GETCURSEL (Коммктрл. h)
description: Извлекает текущую выбранную дату. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- элементы управления Windows сообщений MCM_GETCURSEL
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
ms.openlocfilehash: b40ed6797cd7f40eb68e40a9eac90eb250badd461011e5490c0f4c8473571bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170211"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Время в элементе управления ' календарь на месяц '](month-calendar-controls.md)
</dt> </dl>

 

