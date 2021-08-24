---
description: Вызывается источником мультимедиа при запуске нового потока.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Событие Меневстреам (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499b7899c499e87a45e9b7f043db94724b41d729d3b836e7c9f8d71d83616841
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228774"
---
# <a name="menewstream-event"></a>Событие Меневстреам

Вызывается источником мультимедиа при запуске нового потока.

Когда метод [**имфмедиасаурце:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) вызывается для источника мультимедиа, источник мультимедиа отправляет одно событие для каждого выбранного потока:

-   Источник отправляет событие Меневстреам, если поток не был выбран в предыдущем вызове [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), или это самый первый вызов для **запуска** в этом источнике мультимедиа.

-   Источник отправляет событие [меупдатедстреам](meupdatedstream.md) , если поток уже был выбран в предыдущем вызове [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

Для невыбранных потоков события не отправляются.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE                | Описание                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ Unknown<br/> | Содержит указатель на интерфейс [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) потока.<br/> <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




