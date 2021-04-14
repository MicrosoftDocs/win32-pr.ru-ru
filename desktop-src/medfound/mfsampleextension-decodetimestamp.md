---
description: Содержит отметку времени расшифровки (DTS) для образца.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Атрибут MFSampleExtension_DecodeTimestamp (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692590"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>Мфсампликстенсион \_ декодетиместамп, атрибут

Содержит отметку времени расшифровки (DTS) для образца.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Комментарии

Значение атрибута — это DTS в 100-наносекундных единицах. DTS определяется в некоторых стандартах кодирования, включая MPEG. DTS определяет, когда закодированный рисунок должен быть декодирован. Если закодированное видео содержит кадры B, то службы DTS могут отличаться от времени презентации, так как в битовый поток рисунки в формате B отображаются в некотором порядке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> </dl>

 

 




