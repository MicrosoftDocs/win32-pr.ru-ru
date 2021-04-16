---
description: Вызывается модулем подготовки звука при изменении значка сеанса звука.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Событие Меаудиосессионикончанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719384"
---
# <a name="meaudiosessioniconchanged-event"></a>Событие Меаудиосессионикончанжед

Вызывается модулем подготовки звука при изменении значка сеанса звука.

Сеанс мультимедиа перенаправляет это событие в приложение.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE                | Описание                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ пуст<br/>   | Нет данных события.<br/> <br/>                                                     |
| VT \_ Unknown<br/> | Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Комментарии

Это событие отправляется приемником потока модуля подготовки звука. Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: ониконпасчанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) из сеанса аудио.

Чтобы получить новый значок, вызовите метод [**имфаудиополици:: жетиконпас**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имфаудиополици:: Жетиконпас**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Потоковая прорисовка звука](streaming-audio-renderer.md)
</dt> </dl>

 

 
