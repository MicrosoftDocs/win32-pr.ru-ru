---
description: Указывает, какие звуковые устройства использует DSP для записи и визуализации звука.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Свойство MFPKEY_WMAAECMA_DEVICE_INDEXES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898206"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>\_ \_ \_ Свойство индексов устройства мфпкэй вмааекма

Указывает, какие звуковые устройства использует DSP для записи и визуализации звука.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

(-1,-1).

## <a name="applies-to"></a>Применение

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Комментарии

Задайте это свойство при использовании DSP в режиме исходного кода. DSP игнорирует это свойство в режиме фильтрации.

Значение свойства — 2 16-разрядное **слово**, упакованное в **DWORD**. Верхние 16 бит указывают устройство отрисовки звука (обычно это докладчик), а младшие 16 бит указывают устройство записи (обычно это микрофон). Каждое устройство указывается в виде индекса в коллекции звуковых устройств. Если индекс равен-1, используется устройство по умолчанию.

Индекс устройства соответствует индексу коллекции, используемому в интерфейсе [**иммдевицеколлектион**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . Приложение должно воспроизводить высокопроизводительный Voice через выбранное устройство рендеринга. (В конце концов, это голосовая связь пользователя на другом конце телефонной линии, которая воспроизводится на компьютере пользователя.) Если выбранное устройство отрисовки не имеет активного потока, то DSP не сможет обработать выходные данные.

Значение этого свойства по умолчанию равно (-1,-1).

В следующем примере показано, как инициализировать **пропвариант** для этого свойства.


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



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

 

 
