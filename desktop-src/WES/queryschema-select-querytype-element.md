---
title: Элемент SELECT (QueryType)
description: Запрос XPath, определяющий события, включаемые в результирующий набор запроса.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Выбор журнала элементов
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b38a4f24746425bcdbea845b1c23ea5dadfdbcbefa41ebc5fa502147aba2ec67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587407"
---
# <a name="select-querytype-element"></a>Элемент SELECT (QueryType)

Запрос XPath, определяющий события, включаемые в результирующий набор запроса.

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

Элемент **SELECT** определяется сложным типом [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя | Тип   | Описание                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Путь | anyURI | Имя канала или путь к файлу журнала, содержащему события.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>       |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Запрос (Куерилисттипе)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





