---
title: Binary (Евентдататипе), элемент
description: Двоичный BLOB-объект данных для событий, записываемых с помощью ведения журнала событий.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- Журнал событий двоичного элемента
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 495310a46a314b944b29eeb2433b7c5581136c6923c5630d8f09486a95e47fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120402"
---
# <a name="binary-eventdatatype-element"></a>Binary (Евентдататипе), элемент

Двоичный BLOB-объект данных для событий, записываемых с помощью [ведения журнала событий](/windows/desktop/EventLog/event-logging).

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

Элемент **binary** определяется сложным типом [**евентдататипе**](eventschema-eventdatatype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

