---
description: Вызывается потоком мультимедиа при завершении потока.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Событие Миндофстреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23a2db351d31558a617b72a8640d121b71c866021063d4791d19797108f34819
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877777"
---
# <a name="meendofstream-event"></a>Событие Миндофстреам

Вызывается потоком мультимедиа при завершении потока.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Remarks

Когда [сеанс мультимедиа](media-session.md) получает событие миндофстреам, он вызывает [**Имфстреамсинк::P лацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) в соответствующем приемнике носителя с типом маркера **мфстреамсинк \_ маркеров \_ ендофсегмент** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




