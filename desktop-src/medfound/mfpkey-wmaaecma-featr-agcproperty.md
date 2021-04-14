---
description: Указывает, выполняет ли DSP для записи речи автоматический контроль усиления.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: Свойство MFPKEY_WMAAECMA_FEATR_AGC (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692605"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>МФПКЭЙ \_ вмааекма \_ феатр \_ АГК, свойство

Указывает, выполняет ли DSP для записи речи автоматический контроль усиления.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

Логическое значение VT \_

## <a name="default-value"></a>Значение по умолчанию

ВАРИАНТ \_ false

## <a name="applies-to"></a>Применение

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Комментарии

Автоматический усиление контроля — это компонент DSP, который корректирует прибыль таким образом, чтобы уровень вывода сигнала оставался в том же приближенном диапазоне.

Это свойство может иметь следующие значения.



| Значение          | Описание                     |
|----------------|---------------------------------|
| ВАРИАНТ \_ false | Отключить автоматический контроль усиления. |
| ВАРИАНТ \_ true  | Включить автоматический контроль усиления.  |



 

По умолчанию это свойство имеет значение VARIANT \_ false (отключено). Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.

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

 

 
