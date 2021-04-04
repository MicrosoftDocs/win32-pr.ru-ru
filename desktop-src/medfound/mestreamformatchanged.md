---
description: Вызывается потоком мультимедиа при изменении типа мультимедиа потока.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Событие Местреамформатчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898370"
---
# <a name="mestreamformatchanged-event"></a>Событие Местреамформатчанжед

Вызывается потоком мультимедиа при изменении типа мультимедиа потока.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE                | Описание                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| VT \_ Unknown<br/> | Указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) нового типа носителя.<br/> <br/> |



## <a name="remarks"></a>Комментарии

Это событие используется для сигнализации изменений формата в потоке.

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

 

 




