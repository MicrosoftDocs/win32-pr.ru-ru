---
description: Сообщает, что текущий номер потока субтитров изменен для основного заголовка.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 21549ec6427b82c6d229d2e3962689bc8879815429f3a68fd32d54283c30d6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639774"
---
# <a name="ec_dvd_subpicture_stream_change"></a>\_ \_ изменение потока подизображений EC DVD \_ \_

Сообщает, что текущий номер потока субтитров изменен для основного заголовка.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение **типа DWORD** , указывающее на новый номер потока субтитров пользователей. Число потоков субтитров в диапазоне от 0 до 31. Поток 0xFFFFFFFF указывает, что поток не выбран.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Логическое значение, указывающее состояние включения или отключения подизображения.

</dd> </dl>

## <a name="remarks"></a>Remarks

Подизображение может автоматически изменяться при помощи команды навигации, созданной на диске, а также через Управление приложениями с помощью [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).

Это событие возникает во всех доменах.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Двдевкоде. h (включение DShow. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> <dt>

[Коды уведомлений о событиях DVD](dvd-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




