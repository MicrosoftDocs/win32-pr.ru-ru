---
description: Вызывается приемником потока при завершении перехода в приостановленное состояние.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Событие Местреамсинкпаусед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702613"
---
# <a name="mestreamsinkpaused-event"></a>Событие Местреамсинкпаусед

Вызывается приемником потока при завершении перехода в приостановленное состояние. Переход на приостановку происходит, когда метод [**имфпресентатионклокк::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) вызывается в часах представления приемника.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



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

 

 




