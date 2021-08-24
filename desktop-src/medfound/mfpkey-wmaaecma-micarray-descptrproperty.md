---
description: Задает геометрию массива микрофона для схемы DSP для записи голоса.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Свойство MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2bf0b495e7b57ba60cf5cc993b85a143836c8666e06d6b849ece3693b2a334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722948"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>МФПКЭЙ \_ вмааекма \_ микаррай \_ дескптр, свойство

Задает геометрию массива микрофона для схемы DSP для записи голоса.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

\_большой двоичный объект VT

## <a name="applies-to"></a>Применяется к

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Remarks

Значение этого свойства представляет собой [**ксаудионую \_ \_ \_ геометрическую структуру массива MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) . Эта структура определена в файле заголовка Ксмедиа. h. Чтобы получить геометрию для массива микрофона, запросите звуковое устройство \_ для \_ свойства Geometry для массива MIC кспроперти Audio, \_ \_ вызвав метод **иксконтрол:: кспроперти** на устройстве. дополнительные сведения о массивах микрофонов см. в техническом документе [создание и использование массивов microphone для Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Задайте это свойство, если вы используете DSP в режиме фильтрации, а обработка массивов микрофонов включена. При использовании DSP в режиме исходного кода DSP автоматически запрашивает у устройства сведения о геометрических данных.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP для записи речи](voicecapturedmo.md)
</dt> </dl>

 

 
