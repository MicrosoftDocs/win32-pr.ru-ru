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
ms.openlocfilehash: da027136deed48a97b2ea9384bc37a1a45d00650d90b8fd855ea8226e58583aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343650"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





