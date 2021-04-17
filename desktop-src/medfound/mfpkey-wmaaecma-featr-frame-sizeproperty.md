---
description: Указывает размер звукового кадра, используемого DSP записи речи.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Свойство MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692603"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Размер кадра

Указывает размер звукового кадра, используемого DSP записи речи.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="applies-to"></a>Применение

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Комментарии

Алгоритм "Отмена акустического эха" обрабатывает образцы звука PCM по одному кадру за раз. Значение этого свойства равно размеру звукового кадра в образцах. Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.

DSP для захвата голоса поддерживает следующие размеры кадров:

-   80
-   128
-   160
-   240
-   256
-   320

Если значение этого свойства равно нулю, то DSP выбирает размер кадра в зависимости от системного режима и формата выходных данных.

Однако для лучшей производительности рекомендуется, чтобы приложения использовали значение по умолчанию. Если режимом обработки является только массив микрофонов, значение по умолчанию — 320. Для всех остальных режимов обработки значение по умолчанию — 160 выборки. Дополнительные сведения о режимах обработки для схемы DSP для записи голоса см. в разделе [ \_ \_ \_ режим системы мфпкэй вмааекма](mfpkey-wmaaecma-system-modeproperty.md).

После первого вызова [**имедиаобжект:: аллокатестреамингресаурцес**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) или [**Имедиаобжект::P роцессаутпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)можно прочитать это свойство, чтобы получить фактический размер кадра, даже если в [**\_ \_ \_ режиме мфпкэй вмааекма функции**](mfpkey-wmaaecma-feature-modeproperty.md) задано значение false.

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

 

 
