---
description: Посылается асинхронным Media Foundation преобразованием (MFT), когда новые выходные данные доступны из MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Событие Метрансформхавеаутпут (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673343"
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

## <a name="remarks"></a>Комментарии

Асинхронный МФТС отправляет это событие через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Синхронное МФТС никогда не отправляет это событие.

Когда клиент MFT получает это событие, он должен вызвать [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , чтобы получить выходные данные.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                               |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Асинхронный МФТС](asynchronous-mfts.md)
</dt> </dl>

 

 




