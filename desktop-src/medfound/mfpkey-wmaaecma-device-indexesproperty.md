---
description: Указывает, какие звуковые устройства использует DSP для записи и визуализации звука.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Свойство MFPKEY_WMAAECMA_DEVICE_INDEXES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e9fd9eae8d53f1fa19bd8b55d94d292b9cd6cbf214b7a71a6473f1af647f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873003"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>\_ \_ \_ Свойство индексов устройства мфпкэй вмааекма

Указывает, какие звуковые устройства использует DSP для записи и визуализации звука.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

(-1,-1).

## <a name="applies-to"></a>Применяется к

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Remarks

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP для записи речи](voicecapturedmo.md)
</dt> </dl>

 

 
