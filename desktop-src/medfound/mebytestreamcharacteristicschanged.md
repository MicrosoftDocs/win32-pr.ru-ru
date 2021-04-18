---
description: Отправляется потоком байтов при изменении характеристик потока байтов.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Событие Мебитестреамчарактеристиксчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719406"
---
# <a name="mebytestreamcharacteristicschanged-event"></a>Событие Мебитестреамчарактеристиксчанжед

Отправляется потоком байтов при изменении характеристик потока байтов.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE               | Описание                           |
|-----------------------|---------------------------------------|
| VT \_ пуст <br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Комментарии

Это событие означает, что изменилась одна или несколько из следующих характеристик:

-   Флаги возможностей ([**имфбитестреам:: Capabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))
-   Флаг конца потока ([**имфбитестреам:: исендофстреам**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))
-   Length ([**имфбитестреам:: DATALENGTH**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))

Это событие поддерживают не все реализации [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) . Чтобы получить событие, запросите объект байтового потока для интерфейса [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




