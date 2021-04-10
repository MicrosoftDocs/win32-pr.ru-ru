---
title: Сложный тип Метадататипе
description: Определяет типы метаданных, которые можно определить в разделе метаданных манифеста.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Журнал событий сложных типов Метадататипе
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071981"
---
# <a name="metadatatype-complex-type"></a>Сложный тип Метадататипе

Определяет типы метаданных, которые можно определить в разделе метаданных манифеста.

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                       | Тип                                                                       | Описание                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**канала**](eventmanifestschema-channels-metadatatype-element.md)         | [**чаннеллисттипе**](eventmanifestschema-channellisttype-complextype.md) | Определяет список каналов, к которым поставщики могут регистрировать события. Затем поставщик может импортировать один или несколько каналов в своем манифесте.<br/>               |
| [**словами**](eventmanifestschema-keywords-metadatatype-element.md)         | [**кэйвордлисттипе**](eventmanifestschema-keywordlisttype-complextype.md) | Определяет список ключевых слов, которые определяют категорию событий, записываемых поставщиком.<br/>                                                            |
| [**Выравнивание**](eventmanifestschema-levels-metadatatype-element.md)             | [**левеллисттипе**](eventmanifestschema-levellisttype-complextype.md)     | Определяет список уровней, указывающих серьезность события.<br/>                                                                                       |
| **message**                                                                   |                                                                            | Определяет строку сообщения.<br/>                                                                                                                             |
| **мессажетабле**                                                              |                                                                            | Определяет список строк сообщений.<br/>                                                                                                                    |
| [**намедкуериес**](eventmanifestschema-namedqueries-metadatatype-element.md) | [**намедкуеритипе**](eventmanifestschema-namedquerytype-complextype.md)   | Определяет список именованных запросов, использующих регулярные выражения для выполнения операций поиска и замены в строке сообщения события.<br/>                        |
| [**коды операций**](eventmanifestschema-opcodes-metadatatype-element.md)           | [**опкоделисттипе**](eventmanifestschema-opcodelisttype-complextype.md)   | Определяет список кодов операций, которые можно использовать для группирования событий в задаче.<br/>                                                                             |
| **операции**                                                                     | [**тасклисттипе**](eventmanifestschema-tasklisttype-complextype.md)       | Определяет список задач, которые поставщик может использовать для группирования событий. Как правило, задачи используются для группирования событий для компонента или компонента поставщика.<br/> |
| [**типов**](eventmanifestschema-types-metadatatype-element.md)               | [**типелисттипе**](eventmanifestschema-typelisttype-complextype.md)       | Определяет список типов XML.<br/>                                                                                                                          |



## <a name="attributes"></a>Атрибуты



| Имя    | Тип                                                              | Описание                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| message | [**стртаблереф**](eventmanifestschema-strtableref-simpletype.md) | Ссылка на локализованную строку в таблице строк.<br/>                                |
| mid     | xs:string                                                         | Не используется.<br/>                                                                               |
| name    | anyURI                                                            | URI мета файла. <br/>                                                              |
| символ  | [**ксимболтипе**](eventmanifestschema-csymboltype-simpletype.md) | Символьное имя, создаваемое компилятором сообщений для этой строки сообщения.<br/> |
| значение   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Число, используемое в качестве идентификатора сообщения для данного сообщения.<br/>                           |



## <a name="remarks"></a>Комментарии

Несмотря на то, что можно создать манифест, содержащий раздел метаданных, служба не будет использовать ее. единственными метаданными, распознаваемыми службой, являются метаданные, найденные в файле Winmeta.xml.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





