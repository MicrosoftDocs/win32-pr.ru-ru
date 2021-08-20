---
description: Отправляется Имфмедиасаурце, который инкапсулирует устройство, чтобы указать, что устройство было вытеснено.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Событие Мевидеокаптуредевицепримптед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78246d6560344735167fc6efd45ba0481095534977c67dac11a76ffae0947d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061167"
---
# <a name="mevideocapturedevicepreempted-event"></a>Событие Мевидеокаптуредевицепримптед

Отправляется [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , который инкапсулирует устройство, чтобы указать, что устройство было вытеснено.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE               | Описание                           |
|-----------------------|---------------------------------------|
| VT \_ пуст <br/> | Нет данных события.<br/> <br/> |



## <a name="remarks"></a>Remarks

Это событие отправляется [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) , который инкапсулирует устройство.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




