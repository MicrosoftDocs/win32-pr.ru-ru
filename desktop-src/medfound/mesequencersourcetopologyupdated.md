---
description: 'Вызывается источником Sequencer, когда метод Имфсекуенцерсаурце:: Упдатетопологи завершается асинхронно.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Событие Месекуенцерсаурцетопологюпдатед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711568"
---
# <a name="mesequencersourcetopologyupdated-event"></a>Событие Месекуенцерсаурцетопологюпдатед

Вызывается источником Sequencer, когда метод [**имфсекуенцерсаурце:: упдатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) завершается асинхронно.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE            | Описание                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UI4<br/> | Идентификатор элемента Sequencer для обновляемой топологии. Приложение задает это значение в параметре *ДВИД* метода [**упдатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .<br/> <br/> |



## <a name="remarks"></a>Комментарии

Это событие сигнализирует, что источник Sequencer обновил топологию, но не означает, что топология готова к воспроизведению. Приложение должно ожидать события [месессионтопологистатус](mesessiontopologystatus.md) .

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

[Источник Sequencer](sequencer-source.md)
</dt> </dl>

 

 




