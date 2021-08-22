---
description: Вызывается приемником потока при завершении перехода в приостановленное состояние.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Событие Местреамсинкпаусед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd3e278c4aeb72300af5ef3821a465ac493efa554ed86d798716ff6dffbf1ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228604"
---
# <a name="mestreamsinkpaused-event"></a>Событие Местреамсинкпаусед

Вызывается приемником потока при завершении перехода в приостановленное состояние. Переход на приостановку происходит, когда метод [**имфпресентатионклокк::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) вызывается в часах представления приемника.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Приемники носителей](media-sinks.md)
</dt> </dl>

 

 




