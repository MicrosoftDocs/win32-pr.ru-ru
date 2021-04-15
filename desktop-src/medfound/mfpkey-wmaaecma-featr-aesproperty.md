---
description: Указывает, сколько раз в DSP для записи голоса выполняется подавление акустического эха (AES) на остаточном сигнале.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: Свойство MFPKEY_WMAAECMA_FEATR_AES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647225"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a>МФПКЭЙ \_ вмааекма \_ феатр \_ AES, свойство

Указывает, сколько раз в DSP для записи голоса выполняется подавление акустического эха (AES) на остаточном сигнале.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="applies-to"></a>Применение

-   [DSP для записи речи](voicecapturedmo.md)

## <a name="remarks"></a>Комментарии

DSP записи голоса могут выполнять алгоритм AES в остаточном сигнале после отмены эха. Это свойство может иметь значение 0, 1 или 2. Значение по умолчанию — 0. Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.

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

 

 
