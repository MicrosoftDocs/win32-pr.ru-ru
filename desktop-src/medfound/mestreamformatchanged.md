---
description: Вызывается потоком мультимедиа при изменении типа мультимедиа потока.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Событие Местреамформатчанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762f65beb26f5095c9e89be845f468e3ca53c9b5cd227916bb7cc38417626c60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957274"
---
# <a name="mestreamformatchanged-event"></a>Событие Местреамформатчанжед

Вызывается потоком мультимедиа при изменении типа мультимедиа потока.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE                | Описание                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| VT \_ Unknown<br/> | Указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) нового типа носителя.<br/> <br/> |



## <a name="remarks"></a>Remarks

Это событие используется для сигнализации изменений формата в потоке.

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

 

 




