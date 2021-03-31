---
description: 'Вызывается источником мультимедиа при изменении частоты воспроизведения. Это событие отправляется после асинхронного завершения метода Имфратеконтрол:: Сетрате.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Событие Месаурцератечанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154655"
---
# <a name="mesourceratechanged-event"></a>Событие Месаурцератечанжед

Вызывается источником мультимедиа при изменении частоты воспроизведения. Это событие отправляется после асинхронного завершения метода [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) .

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE           | Описание                                   |
|-------------------|-----------------------------------------------|
| VT \_ R4<br/> | Новая скорость воспроизведения.<br/> <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Реализация управления скоростью](implementing-rate-control.md)
</dt> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Управление скоростью](rate-control.md)
</dt> <dt>

[**Имфратеконтрол:: Сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




