---
description: Вызывается объектом включения содержимого при завершении действия "объекты".
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Событие Минаблеркомплетед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155591"
---
# <a name="meenablercompleted-event"></a>Событие Минаблеркомплетед

Вызывается объектом включения содержимого при завершении действия по включению объекта. Это событие может вызываться объектами, которые предоставляют интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . Событие возникает, если происходит одно из следующих событий:

-   Метод [**имфконтентенаблер:: аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) завершается асинхронно.
-   Приложение вызывает [**имфконтентенаблер:: мониторенабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), а затем приложение ЗАВЕРШАЕТ запрос HTTP POST, как описано в методе **мониторенабле** .

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Комментарии

Код состояния события может содержать одно из следующих значений.



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ОК**                            | Операция успешно выполнена.                                                                                                                                                        |
| **нотаккуиред лицензия на NS \_ E \_ DRM \_ \_** | Лицензия DRM не была получена. Если предыдущая попытка использовала [**аутоматиценабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), приложение должно попытаться не выполнять автоматическое получение. |
| **\_ \_ монитор DRM NS \_ S \_ отменен**   | Операция [**мониторенабле**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) была отменена.                                                                                            |



 

Чтобы получить это событие, запросите интерфейс [**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Затем вызовите [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), как описано в разделе [генераторы событий мультимедиа](media-event-generators.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфконтентенаблер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Генераторы событий мультимедиа](media-event-generators.md)
</dt> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




