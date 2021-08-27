---
description: Отправляется источником записи звука при удалении устройства.
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: Событие Мекаптуреаудиосессиондевицеремовед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1c3b0e9acbf627800f69ad8ba374edc4b6f075268e61d2c71618c07e8c95645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114204"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a>Событие Мекаптуреаудиосессиондевицеремовед

Отправляется источником записи звука при удалении устройства.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE               | Описание                           |
|-----------------------|---------------------------------------|
| VT \_ пуст <br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Remarks

Это событие отправляется потоком мультимедиа источника записи звука.

Источник захвата отправляет это событие при получении события [**иаудиосессионевентс:: онсессиондисконнектед**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) из сеанса аудио с причиной отключения соединения, равной **дисконнектреасондевицеремовал**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 
