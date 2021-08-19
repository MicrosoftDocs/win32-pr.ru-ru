---
description: Вызывается модулем подготовки звука при изменении значка сеанса звука.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Событие Меаудиосессионикончанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce466cf88b93c9cf806a2a6b70f76b084e8aa0b2c8fb2910a7391337a13b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062463"
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



## <a name="remarks"></a>Remarks

Это событие отправляется приемником потока модуля подготовки звука. Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: ониконпасчанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) из сеанса аудио.

Чтобы получить новый значок, вызовите метод [**имфаудиополици:: жетиконпас**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Имфаудиополици:: Жетиконпас**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Потоковая прорисовка звука](streaming-audio-renderer.md)
</dt> </dl>

 

 
