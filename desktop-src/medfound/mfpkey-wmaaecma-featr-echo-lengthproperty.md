---
description: Указывает продолжительность эхо-запроса, который алгоритм AEC может обрабатывать (в миллисекундах).
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: Свойство MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692604"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a>МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Длина эхо

Указывает продолжительность эхо-запроса, который алгоритм AEC может обрабатывать (в миллисекундах).

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

256

## <a name="applies-to"></a>Применение

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Комментарии

Алгоритм AEC использует адаптивный фильтр, длина которого определяется длительностью эха. Рекомендуется, чтобы приложения использовали одно из следующих значений:

-   128
-   256
-   512
-   1024

Значение по умолчанию — 256 миллисекунд, что достаточно для большинства офисных и домашних сред. Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.

DSP использует это свойство только в том случае, если включена обработка AEC.

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

 

 
