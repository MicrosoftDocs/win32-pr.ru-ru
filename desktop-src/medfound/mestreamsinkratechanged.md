---
description: Вызывается приемником потока при изменении скорости.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Событие Местреамсинкратечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712413"
---
# <a name="mestreamsinkratechanged-event"></a>Событие Местреамсинкратечанжед

Вызывается приемником потока при изменении скорости.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Комментарии

Если приемник потока поддерживает изменение частоты, он отправляет это событие после завершения изменения скорости. Событие отправляется один раз для каждого вызова метода [**имфклоккстатесинк:: онклокксетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) приемника. Если изменение скорости не прошло успешно, значение состояния события является кодом ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Приемники носителей](media-sinks.md)
</dt> </dl>

 

 




