---
description: Вызывается потоком мультимедиа, когда метод Имфмедиасаурце::P Аусе завершается асинхронно.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: Событие Местреампаусед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711215"
---
# <a name="mestreampaused-event"></a>Событие Местреампаусед

Вызывается потоком мультимедиа, когда метод [**имфмедиасаурце::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) завершается асинхронно.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Комментарии

Каждый активный поток в презентации отправляет это событие.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




