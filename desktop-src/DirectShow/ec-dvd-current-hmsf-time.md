---
description: Сигнализирует о текущем времени в формате хмсф времени (DVD-диск \_ \_ ) относительно начала заголовка. Это событие активируется в начале каждого ВОБУ, что происходит каждые 0,4 – 1,0 секунд.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685199"
---
# <a name="ec_dvd_current_hmsf_time"></a>\_ \_ текущее \_ хмсф \_ время в формате EC DVD

Сигнализирует о текущем времени в формате [**\_ хмсф времени \_ (DVD-диск**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) ) относительно начала заголовка. Это событие активируется в начале каждого ВОБУ, что происходит каждые 0,4 – 1,0 секунд.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение типа ULONG, содержащее структуру времени \_ ХМСФ DVD \_ . Назначьте lParam1 переменной ULONG, а затем приведите эту переменную к DVD-хмсф времени, \_ \_ чтобы получить доступ к его значениям.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Значение типа ULONG, содержащее объединение [**\_ \_ флагов**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)времени в формате DVD.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Формат времени выполнения \_ ХМСФ DVD \_ предназначен для замены старого формата BCD, возвращаемого в \_ \_ событиях текущего времени в формате "DVD" в формате EC \_ . Коды времени ХМСФ проще работать с. Чтобы в навигаторе отправлялись \_ \_ текущие \_ события хмсф времени EC для DVD \_ , а не для \_ \_ \_ событий текущего времени в формате DVD, приложение должно вызвать `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` . Если этот флаг установлен, навигатор также будет предполагать, что все параметры времени в методах [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) и [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) передаются как коды времени DVD \_ хмсф \_ .

Это событие возникает в доменах заголовков.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Двдевкоде. h (включение DShow. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> <dt>

[Коды уведомлений о событиях DVD](dvd-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




