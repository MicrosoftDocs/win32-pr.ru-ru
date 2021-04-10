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
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071134"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

