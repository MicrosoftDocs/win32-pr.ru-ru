---
title: Элемент System (EventType)
description: Содержит сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- Журнал событий системного элемента
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85f20b364998fb34f3fe9eb6973770b414de501b60e34df6f97a607acb494947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588191"
---
# <a name="system-eventtype-element"></a>Элемент System (EventType)

Содержит сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

Элемент **System** определяется сложным типом [**EventType**](eventschema-eventtype-complextype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**событие**](eventschema-event-element.md)
</dt> </dl>

 

 





