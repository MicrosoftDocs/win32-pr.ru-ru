---
description: Вызывается сетевым источником при открытии URL-адреса.
ms.assetid: 0844ac10-cc5b-4e7f-92df-3a5901c72148
title: Событие Меконнектстарт (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01360d452e6b20bde9e7aaaaf9e678cab1b3c6fe912e9682949dfc24e1e7d5cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013854"
---
# <a name="meconnectstart-event"></a>Событие Меконнектстарт

Вызывается сетевым источником при открытии URL-адреса.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Remarks

Источник сети отправляет это событие непосредственно в приложение через метод [**имфсаурцеопенмонитор:: онсаурцеевент**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) приложения, а не через обычный интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфсаурцеопенмонитор**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




