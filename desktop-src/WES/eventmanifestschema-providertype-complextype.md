---
title: Сложный тип ProviderType
description: Определяет поставщик и метаданные, используемые для определения его событий. | Сложный тип ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Журнал событий сложного типа ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353372"
---
# <a name="providertype-complex-type"></a>Сложный тип ProviderType

Определяет поставщик и метаданные, используемые для определения его событий.

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
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
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                       | Тип                                                                         | Описание                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**канала**](eventmanifestschema-channels-providertype-element.md)         | [**чаннеллисттипе**](eventmanifestschema-channellisttype-complextype.md)   | Определяет список каналов, к которым поставщики могут регистрировать события.<br/>                                                                                                                                                                                      |
| [**событиях**](eventmanifestschema-events-providertype-element.md)             | [**дефинитионтипе**](eventmanifestschema-definitiontype-complextype.md)     | Определяет список определений событий событий, которые поставщик может заносить в журнал.<br/>                                                                                                                                                                       |
| **фильтрующ**                                                                   | [**филтерлисттипе**](eventmanifestschema-filterlisttype-complextype.md)     | Определяет список фильтров, поддерживаемых поставщиком. Можно использовать фильтры, как и ключевые слова, чтобы определить, нужно ли создавать событие. <br/> **Windows Server 2008 и Windows Vista:** Не поддерживается до Windows 7.<br/> |
| [**словами**](eventmanifestschema-keywords-providertype-element.md)         | [**кэйвордлисттипе**](eventmanifestschema-keywordlisttype-complextype.md)   | Определяет список ключевых слов, которые классифицируют события.<br/>                                                                                                                                                                                                 |
| [**Выравнивание**](eventmanifestschema-levels-providertype-element.md)             | [**левеллисттипе**](eventmanifestschema-levellisttype-complextype.md)       | Определяет список уровней, указывающих серьезность события.<br/>                                                                                                                                                                                    |
| [**указания**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | Определяет список пар "имя-значение", на которые можно ссылаться в разделе шаблона манифеста.<br/>                                                                                                                                                 |
| [**намедкуериес**](eventmanifestschema-namedqueries-providertype-element.md) | [**намедкуеритипе**](eventmanifestschema-namedquerytype-complextype.md)     | Не используется. Определяет список именованных запросов, которые запрашивают строку сообщения о событии для значения и выполняют указанное действие, если оно найдено.<br/>                                                                                                                 |
| [**коды операций**](eventmanifestschema-opcodes-providertype-element.md)           | [**опкоделисттипе**](eventmanifestschema-opcodelisttype-complextype.md)     | Определяет список кодов операций, которые можно использовать для группирования событий в задаче.<br/>                                                                                                                                                                          |
| [**операции**](eventmanifestschema-tasks-providertype-element.md)               | [**тасклисттипе**](eventmanifestschema-tasklisttype-complextype.md)         | Определяет список задач, которые поставщик может использовать для группирования событий. Как правило, задачи используются для группирования событий для компонента или компонента поставщика.<br/>                                                                                              |
| [**шаблоны**](eventmanifestschema-templates-providertype-element.md)       | [**темплателисттипе**](eventmanifestschema-templatelisttype-complextype.md) | Определяет список шаблонов, указывающих данные, включаемые в события.<br/>                                                                                                                                                                      |



## <a name="attributes"></a>Атрибуты



| Имя                                | Тип                                                              | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**гуидтипе**](eventmanifestschema-guidtype-simpletype.md)       | Идентификатор GUID, который однозначно идентифицирует поставщик.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| helpLink                            | anyURI                                                            | Ссылка на URL-адрес или MS Help на содержимое, содержащее сведения о событиях, которые вызывает поставщик.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**стртаблереф**](eventmanifestschema-strtableref-simpletype.md) | Локализованное отображаемое имя для поставщика. Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста. <br/>                                                                                                                                                                                                                                                                                                                           |
| мессажефиленаме                     | [**Равно**](eventmanifestschema-filepath-simpletype.md)       | Полный путь к файлу, содержащему ресурсы локализованного сообщения поставщика. Файл может быть исполняемым файлом или DLL-файлом.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| name                                | anyURI                                                            | Имя поставщика. Имя должно иметь форму,  -  - *компонент* продукта компании.<br/> Имя не может быть длиннее 255 символов и не может содержать символы: ">", "<", "&", "" "," "," \| \\ ",": "," ","? "," \* "или символы с кодами меньше 31. Кроме того, имя должно соответствовать общим ограничениям на имена файлов и разделов реестра. Эти ограничения можно найти по [имени файла](/windows/desktop/FileIO/naming-a-file)и [ограничению размера элементов реестра](/windows/desktop/SysInfo/registry-element-size-limits).<br/> |
| параметерфиленаме                   | [**Равно**](eventmanifestschema-filepath-simpletype.md)       | Полный путь к файлу, содержащему строковые ресурсы параметра поставщика. Файл может быть исполняемым файлом или DLL-файлом. Можно указать более одного файла параметров, разделяя их точкой с запятой. Файл ищется, если строка сообщения события содержит строку параметра. Параметры позволяют предоставлять локализуемые строки вставки. Дополнительные сведения см. в разделе "Примечания".<br/>                                                                                                                                                |
| ресаурцефиленаме                    | [**Равно**](eventmanifestschema-filepath-simpletype.md)       | Полный путь к файлу, содержащему ресурсы метаданных поставщика. Файл может быть исполняемым файлом или DLL-файлом.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | Только для внутреннего использования.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| символ                              | [**ксимболтипе**](eventmanifestschema-csymboltype-simpletype.md) | Символ, используемый для ссылки на идентификатор GUID поставщика в приложении. [**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для идентификатора GUID поставщика в файле заголовка, создаваемом компилятором.<br/>                                                                                                                                                                                                                                                                           |
| варнонаппликатионкомпатибилитеррор | **xs:boolean**                                                    | Только для внутреннего использования.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>Комментарии

Просмотр событий Windows (Eventvwr.exe) будет использовать локализованную строку сообщения, если она доступна; в противном случае используется строка из атрибута Name.

Пути для Ресаурцефиленаме, Мессажефиленаме и Параметерфиленаме могут содержать переменные среды. Если вы определили новую переменную среды для использования в пути, необходимо перезагрузить компьютер, чтобы служба журнала событий могла выбрать новую переменную. в противном случае служба не сможет найти ресурсы поставщика.

Строка сообщения события может содержать строки вставки и строки параметров. Строка вставки имеет форму%*n*, где *n* — это Отсчитываемый от единицы индекс, определяющий элемент данных из шаблона данных события, который необходимо вставить в сообщение. Строка параметра (см. атрибут **параметерфиленаме** ) имеет вид%%*n*, где n — это идентификатор сообщения в таблице сообщений. Если строка сообщения события содержит "%1% %11 = %2% %12", а значения элементов данных для %1 и %2 — 8 и 2, соответственно, а строки параметров для% %11 и %12 были "кварты" и "галлоны" соответственно, отформатированная строка будет иметь значение "8 кварт = 2 галлоны".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

