---
description: Посылается асинхронным Media Foundation преобразованием (MFT), когда новые выходные данные доступны из MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Событие Метрансформхавеаутпут (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bed68da623c3fed0bced01e32003dfa0c7625b9be8863644d2bf9486122c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061228"
---
# <a name="metransformhaveoutput-event"></a>Событие Метрансформхавеаутпут

Посылается асинхронным Media Foundation преобразованием (MFT), когда новые выходные данные доступны из MFT.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание               |
|----------------------|---------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> |



## <a name="attributes"></a>Атрибуты

Для этого события не определены атрибуты.

## <a name="remarks"></a>Remarks

Асинхронный МФТС отправляет это событие через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Синхронное МФТС никогда не отправляет это событие.

Когда клиент MFT получает это событие, он должен вызвать [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , чтобы получить выходные данные.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                               |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                  |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Асинхронный МФТС](asynchronous-mfts.md)
</dt> </dl>

 

 




