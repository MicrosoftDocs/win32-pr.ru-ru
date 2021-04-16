---
description: Задает геометрию массива микрофона для схемы DSP для записи голоса.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Свойство MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692598"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>МФПКЭЙ \_ вмааекма \_ микаррай \_ дескптр, свойство

Задает геометрию массива микрофона для схемы DSP для записи голоса.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

\_большой двоичный объект VT

## <a name="applies-to"></a>Применение

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Комментарии

Значение этого свойства представляет собой [**ксаудионую \_ \_ \_ геометрическую структуру массива MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) . Эта структура определена в файле заголовка Ксмедиа. h. Чтобы получить геометрию для массива микрофона, запросите звуковое устройство \_ для \_ свойства Geometry для массива MIC кспроперти Audio, \_ \_ вызвав метод **иксконтрол:: кспроперти** на устройстве. Дополнительные сведения о массивах микрофонов см. в техническом документе [Создание и использование массивов микрофонов для Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Задайте это свойство, если вы используете DSP в режиме фильтрации, а обработка массивов микрофонов включена. При использовании DSP в режиме исходного кода DSP автоматически запрашивает у устройства сведения о геометрических данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP для записи речи](voicecapturedmo.md)
</dt> </dl>

 

 
