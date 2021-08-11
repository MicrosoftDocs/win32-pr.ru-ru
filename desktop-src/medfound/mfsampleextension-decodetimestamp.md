---
description: Содержит отметку времени расшифровки (DTS) для образца.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Атрибут MFSampleExtension_DecodeTimestamp (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d72ea69f487efe24148fa8ce60ad05eb7a124673f02a78e70c67f604a51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241485"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>Мфсампликстенсион \_ декодетиместамп, атрибут

Содержит отметку времени расшифровки (DTS) для образца.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Remarks

Значение атрибута — это DTS в 100-наносекундных единицах. DTS определяется в некоторых стандартах кодирования, включая MPEG. DTS определяет, когда закодированный рисунок должен быть декодирован. Если закодированное видео содержит кадры B, то службы DTS могут отличаться от времени презентации, так как в битовый поток рисунки в формате B отображаются в некотором порядке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> </dl>

 

 




