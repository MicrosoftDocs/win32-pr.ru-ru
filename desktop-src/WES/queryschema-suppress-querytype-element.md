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
ms.openlocfilehash: 2612a98c282627154a9107f2f9f77a3ddb52c191e00dbcb394c8db4d7c796b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032014"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Запрос (Куерилисттипе)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





