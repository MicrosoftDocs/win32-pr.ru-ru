---
description: Указывает тип обнаружения действия голоса, выполняемого DSP.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: Свойство MFPKEY_WMAAECMA_FEATR_VAD (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701812"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>МФПКЭЙ \_ вмааекма \_ феатр \_ Вад, свойство

Указывает тип обнаружения действия голоса, выполняемого DSP.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="applies-to"></a>Применение

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Комментарии

Значение этого свойства является членом перечисления [ \_ Вад \_ режима AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) . Выходными данными при обнаружении голосовой активности является число от 0 до 3, вычисляемое для каждого звукового кадра. DSP кодирует результат в наименьшем бите первых двух звуковых образцов в каждом звуковом кадре. Значение этого параметра зависит от указанного режима.

В следующем коде показано, как извлечь результаты из звуковых данных. В этом примере *паутпут* является указателем на начало звукового кадра в выходных данных.


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



Значение этого свойства по умолчанию равно 0 (отключено). Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
