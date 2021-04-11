---
title: Подавлять (QueryType) элемент
description: Запрос XPath, определяющий события, исключаемые из результирующего набора запроса.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Подавлять элемент EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137666"
---
# <a name="suppress-querytype-element"></a>Подавлять (QueryType) элемент

Запрос XPath, определяющий события, исключаемые из результирующего набора запроса.

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

Элемент **подавлять** определяется сложным типом [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя | Тип   | Описание                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Путь | anyURI | Имя канала или путь к файлу журнала, содержащему события.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Запрос (Куерилисттипе)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





