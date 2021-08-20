---
description: Позволяет приложению переопределять параметры по умолчанию в различных свойствах схемы DSP для записи речи.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: Свойство MFPKEY_WMAAECMA_FEATURE_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e2e4e370876b8ecae91638a4cbe462a4f55e31e8f9e9f525b7b312c04343433
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689322"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a>\_ \_ Свойство режима компонента мфпкэй вмааекма \_

Позволяет приложению переопределять параметры по умолчанию в различных свойствах схемы DSP для записи речи.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

Логическое значение VT \_

## <a name="default-value"></a>Значение по умолчанию

ВАРИАНТ \_ false

## <a name="applies-to"></a>Применяется к

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Remarks

Если это свойство имеет значение VARIANT \_ true, приложение может установить следующие свойства в DSP:

-   [МФПКЭЙ \_ вмааекма \_ феатр \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ АГК](mfpkey-wmaaecma-featr-agcproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ \_](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Длина эхо](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Размер кадра](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ микарр \_ mode](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ микарр \_](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ , \_ Заливка шума](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)
-   [МФПКЭЙ \_ вмааекма \_ феатр \_ Вад](mfpkey-wmaaecma-featr-vadproperty.md)

Если это свойство имеет значение VARIANT \_ false, то DSP игнорирует эти свойства и использует параметры по умолчанию. Значение этого свойства по умолчанию — VARIANT \_ false.

## <a name="requirements"></a>Требования



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

 

 
