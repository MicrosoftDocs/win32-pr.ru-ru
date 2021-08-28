---
description: Вызывается потоком мультимедиа при запуске или при остановке потока. Дополнительные сведения об сужении см. в разделе сведения об управлении скоростью.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Событие Местреамсинмоде (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13a9cc5b625a8b366bece1debc2017fce51e35d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479520"
---
# <a name="mestreamthinmode-event"></a>Событие Местреамсинмоде

Вызывается потоком мультимедиа при запуске или при остановке потока. Дополнительные сведения об *сужении* см. в разделе [сведения об управлении скоростью](about-rate-control.md).

Это событие можно отправить в ответ на метод [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) или метод [**Имфкуалитядвисе:: сетдропмоде**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.




| VARTYPE | Описание | 
|---------|-------------|
| VT_BOOL.<br /> | Указывает, началось ли тонкое начало или прекращение.<br /><ul><li>VARIANT_TRUE: образцы, доставленные после этого события, будут тоньше.</li><li>VARIANT_FALSE: образцы, доставленные после этого события, не будут тоньше.</li></ul><br /> | 




## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




