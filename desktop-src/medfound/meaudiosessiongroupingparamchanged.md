---
description: Вызывается модулем подготовки звука при изменении параметров группирования для сеанса аудио.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Событие Меаудиосессионграупингпарамчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263319"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a>Событие Меаудиосессионграупингпарамчанжед

Вызывается модулем подготовки звука при изменении параметров группирования для сеанса аудио.

Сеанс мультимедиа перенаправляет это событие в приложение.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE                | Описание                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ Unknown<br/> | Указатель на интерфейс [**имфаудиополици**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Комментарии

Это событие отправляется приемником потока модуля подготовки звука. Событие активируется, когда модуль подготовки звука получает событие [**иаудиосессионевентс:: онграупингпарамчанжед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) из сеанса аудио.

Чтобы получить новые параметры группирования, вызовите метод [**имфаудиополици:: жетграупингпарам**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).

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

[**Имфаудиополици:: Жетграупингпарам**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[Потоковая прорисовка звука](streaming-audio-renderer.md)
</dt> </dl>

 

 
