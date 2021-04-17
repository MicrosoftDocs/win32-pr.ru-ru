---
description: Вызывается приемником потока при завершении перехода в состояние выполнения.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Событие Местреамсинкстартед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711563"
---
# <a name="mestreamsinkstarted-event"></a>Событие Местреамсинкстартед

Вызывается приемником потока при завершении перехода в состояние выполнения. Переход на выполнение происходит при вызове метода [**имфпресентатионклокк:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) для часов представления приемника. Приемник мультимедиа получает уведомление через его метод [**имфклоккстатесинк:: онклоккстарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) или [**Имфклоккстатесинк:: онклоккрестарт**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) .

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

 

 




