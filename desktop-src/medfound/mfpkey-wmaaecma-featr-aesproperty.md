---
description: Указывает, сколько раз в DSP для записи голоса выполняется подавление акустического эха (AES) на остаточном сигнале.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: Свойство MFPKEY_WMAAECMA_FEATR_AES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e842bc3064b431437d8bbdfab06c0081ecdb49a8c38288ba4adb78648363c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242041"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a>МФПКЭЙ \_ вмааекма \_ феатр \_ AES, свойство

Указывает, сколько раз в DSP для записи голоса выполняется подавление акустического эха (AES) на остаточном сигнале.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="applies-to"></a>Применяется к

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Remarks

DSP записи голоса могут выполнять алгоритм AES в остаточном сигнале после отмены эха. Это свойство может иметь значение 0, 1 или 2. Значение по умолчанию — 0. Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.

DSP использует это свойство только в том случае, если включена обработка AEC.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP для записи речи](voicecapturedmo.md)
</dt> </dl>

 

 
