---
description: Указывает размер звукового кадра, используемого DSP записи речи.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Свойство MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812a9c7b85a36b730caffe7679cc742a3bc029546a12839afd95a8c8ab58bfeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973293"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Размер кадра

Указывает размер звукового кадра, используемого DSP записи речи.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="applies-to"></a>Применяется к

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Remarks

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

 

 
