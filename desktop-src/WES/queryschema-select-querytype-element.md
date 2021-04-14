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
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416021"
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
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>       |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Родительский элемент**
</dt> <dt>

[**Запрос (Куерилисттипе)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





