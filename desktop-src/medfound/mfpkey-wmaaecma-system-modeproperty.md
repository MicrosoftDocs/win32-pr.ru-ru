---
description: Задает режим обработки для схемы DSP для записи голоса.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Свойство MFPKEY_WMAAECMA_SYSTEM_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662781"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>МФПКЭЙ \_ вмааекма \_ , \_ свойство системного режима

Задает режим обработки для схемы DSP для записи голоса.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="applies-to"></a>Применение

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Комментарии

Значение этого свойства является членом перечисления [ \_ системного \_ режима AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .

Свойство должно иметь одно из следующих значений.



| Значение | Описание                                 |
|-------|---------------------------------------------|
| 0     | Режим "Отмена звукового эха" (AEC)     |
| 2     | Режим только обработки массива микрофона (MAP) |
| 4     | Контекст AEC и режим MAP                            |
| 5     | Ни AEC, ни режим MAP                    |



 

Это свойство необходимо задать перед использованием схемы DSP для записи голоса. После задания этого свойства можно использовать DSP с параметрами по умолчанию или задать дополнительные свойства.

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

 

 
