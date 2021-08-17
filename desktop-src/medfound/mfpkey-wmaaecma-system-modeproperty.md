---
description: Задает режим обработки для схемы DSP для записи голоса.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Свойство MFPKEY_WMAAECMA_SYSTEM_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722b3e502b783f98ef4871cfc6dd184389dfce7f7f942bde1827468e96f5fa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973273"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>МФПКЭЙ \_ вмааекма \_ , \_ свойство системного режима

Задает режим обработки для схемы DSP для записи голоса.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="applies-to"></a>Применяется к

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Remarks

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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP для записи речи](voicecapturedmo.md)
</dt> </dl>

 

 
