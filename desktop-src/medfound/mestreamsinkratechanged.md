---
description: Вызывается приемником потока при изменении скорости.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Событие Местреамсинкратечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43a3a4cbff4464f78e71d3047e2b9ccaddfcbf38adcb5e84bab8f5ae49c5d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827144"
---
# <a name="mestreamsinkratechanged-event"></a>Событие Местреамсинкратечанжед

Вызывается приемником потока при изменении скорости.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Remarks

Если приемник потока поддерживает изменение частоты, он отправляет это событие после завершения изменения скорости. Событие отправляется один раз для каждого вызова метода [**имфклоккстатесинк:: онклокксетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) приемника. Если изменение скорости не прошло успешно, значение состояния события является кодом ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Приемники носителей](media-sinks.md)
</dt> </dl>

 

 




