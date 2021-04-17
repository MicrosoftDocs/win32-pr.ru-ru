---
title: Сложный тип Кэйвордлисттипе
description: Определяет список ключевых слов, которые классифицируют события. | Сложный тип Кэйвордлисттипе
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Журнал событий сложных типов Кэйвордлисттипе
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693997"
---
# <a name="keywordlisttype-complex-type"></a>Сложный тип Кэйвордлисттипе

Определяет список ключевых слов, которые классифицируют события.

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                | Тип                                                               | Описание                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**This**](eventmanifestschema-keyword-keywordlisttype-element.md) | [**кэйвордтипе**](eventmanifestschema-keywordtype-complextype.md) | Определяет ключевое слово, определяющее категорию событий. Можно указать не более 48 ключевых слов.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





