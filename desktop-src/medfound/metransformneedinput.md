---
description: Отправляется асинхронным Media Foundation преобразованием (MFT) для запроса нового входного примера.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Событие Метрансформнидинпут (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc15bdffebfd22b4aecac2818da85e39379f681aec0e12fe92f895824edb78f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013504"
---
# <a name="metransformneedinput-event"></a>Событие Метрансформнидинпут

Отправляется асинхронным Media Foundation преобразованием (MFT) для запроса нового входного примера.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание               |
|----------------------|---------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> |



## <a name="attributes"></a>Атрибуты

Для этого события определены следующие атрибуты.



| attribute                                                                        | Описание                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ \_ \_ ИД входного \_ потока MFT события \_ MF](mf-event-mft-input-stream-id.md)<br/> | Идентификатор потока, для которого требуются входные данные.<br/>*Необходимости*<br/> |



## <a name="remarks"></a>Remarks

Асинхронный МФТС отправляет это событие через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Синхронное МФТС никогда не отправляет это событие.

Когда клиент MFT получает это событие, он должен вызвать [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , чтобы доставить следующий пример. Атрибут [ \_ \_ \_ \_ \_ идентификатора входного потока события MF](mf-event-mft-input-stream-id.md) объекта события указывает, какой входной поток требует данные.

## <a name="requirements"></a>Requirements (Требования)



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

 

 




