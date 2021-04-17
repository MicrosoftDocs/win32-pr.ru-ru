---
title: Сложный тип Намедкуеритипе
description: Не используется. Определяет список именованных запросов, которые запрашивают строку сообщения о событии для значения и выполняют указанное действие, если оно найдено. | Сложный тип Намедкуеритипе
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- Журнал событий сложных типов Намедкуеритипе
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694031"
---
# <a name="namedquerytype-complex-type"></a>Сложный тип Намедкуеритипе

Не используется. Определяет список именованных запросов, которые запрашивают строку сообщения о событии для значения и выполняют указанное действие, если оно найдено.

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                       | Тип                                                                             | Описание                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**паттернмапс**](eventmanifestschema-patternmaps-namedquerytype-element.md) | [**паттернмаплисттипе**](eventmanifestschema-patternmaplisttype-complextype.md) | Определяет список пар регулярных выражений, которые используются для изменения строки сообщения.<br/> |



## <a name="examples"></a>Примеры

В следующем примере показано, как использовать элемент [**намедкуериес**](eventmanifestschema-namedqueries-metadatatype-element.md) . Этот пример принимает содержимое строки сообщения и вставляет его в строку https://www .*мессажестринг*. com. Затем она заменяет строку сообщения на результат. Например, если строка сообщения содержит Microsoft, запрос заменит строку сообщения Майкрософт на https://www.Microsoft.com .


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





