---
description: Вызывается приемником потока после вызова метода Имфстреамсинк::P Лацемаркер.
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: Событие Местреамсинкмаркер (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd6866e8ef1633e4c743d466bb261e194c6ae7253924e34e8c30501b092f415a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228614"
---
# <a name="mestreamsinkmarker-event"></a>Событие Местреамсинкмаркер

Вызывается приемником потока после вызова метода [**имфстреамсинк::P лацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE            | Описание                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| >любой<br/> | Значение события — это копия **пропвариант** , которую вызывающий объект указал в параметре *пварконтекствалуе* метода [**плацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .<br/> <br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Приемники носителей](media-sinks.md)
</dt> </dl>

 

 




