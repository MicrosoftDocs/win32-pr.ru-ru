---
description: Вызывается потоком мультимедиа при завершении потока.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Событие Миндофстреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898386"
---
# <a name="meendofstream-event"></a>Событие Миндофстреам

Вызывается потоком мультимедиа при завершении потока.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Комментарии

Когда [сеанс мультимедиа](media-session.md) получает событие миндофстреам, он вызывает [**Имфстреамсинк::P лацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) в соответствующем приемнике носителя с типом маркера **мфстреамсинк \_ маркеров \_ ендофсегмент** .

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

 

 




