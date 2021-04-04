---
description: Генерируется модулем подготовки звука при изменении отображаемого имени сеанса звука.
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: Событие Меаудиосессионнамечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb06244c196ab55bbd93e12ebff6a6a394176cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810810"
---
# <a name="meaudiosessionnamechanged-event"></a>Событие Меаудиосессионнамечанжед

Генерируется модулем подготовки звука при изменении отображаемого имени сеанса звука.

Сеанс мультимедиа перенаправляет это событие в приложение.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE                | Описание                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ Unknown<br/> | Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Комментарии

Это событие отправляется приемником потока модуля подготовки звука. Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: ондисплайнамечанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) из сеанса аудио.

Чтобы получить новое отображаемое имя, вызовите [**имфаудиополици::**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)lt.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имфаудиополици::/DisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Потоковая прорисовка звука](streaming-audio-renderer.md)
</dt> </dl>

 

 
