---
title: Чтение абстрактной схемы
description: В этом разделе приведен пример кода и рекомендации по чтению из абстрактной схемы, которая предоставляет подмножество данных, хранящихся в объектах attributeSchema и classSchema в контейнере схемы.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- Active Directory схемы, чтение абстрактной схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7095dc4fb5ffe5f11f64781ecd423a60b3d434d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881310"
---
# <a name="reading-the-abstract-schema"></a>Чтение абстрактной схемы

В этом разделе приведен пример кода и рекомендации по чтению из абстрактной схемы, которая предоставляет подмножество данных, хранящихся в объектах **attributeSchema** и **classSchema** в контейнере схемы. Чтобы получить данные, недоступные в абстрактной схеме, прочтите данные непосредственно из контейнера схемы, как описано в разделе [чтение объектов attributeSchema и classSchema](reading-attributeschema-and-classschema-objects.md).

Используйте строку привязки "LDAP://schema" для привязки к указателю [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) в абстрактной схеме. Этот указатель используется для перечисления записей класса, атрибута и синтаксиса в абстрактной схеме. Для получения отдельных записей можно также использовать метод [**иадсконтаинер. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) .


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



Используйте аналогичную строку привязки "LDAP://schema/ &lt; Object &gt; " для непосредственной привязки к записи класса или атрибута в абстрактной схеме. В этой строке " &lt; Object &gt; " — это атрибут **lDAPDisplayName** класса или атрибута. Для классов привязывается к интерфейсу [**иадскласс**](/windows/desktop/api/iads/nn-iads-iadsclass) ; для атрибутов привяжите к интерфейсу [**иадспроперти**](/windows/desktop/api/iads/nn-iads-iadsproperty) .


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



Кроме того, интерфейс [**iAds**](/windows/desktop/api/iads/nn-iads-iads) предоставляет свойство [**iAds. Schema**](/windows/desktop/ADSI/iads-property-methods) . Это свойство возвращает значение ADsPath для класса объекта в формате строки абстрактной привязки схемы. При наличии указателя **iAds** для объекта можно выполнить привязку к его классу в абстрактной схеме, используя значение ADsPath, возвращенное методом **iAds. Schema**.

Для классов в следующей таблице перечислены ключевые свойства, предоставляемые абстрактной схемой.



| Свойство                                                             | Значение                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Иадскласс. abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Указывает, является ли этот класс абстрактным.                                                                                                                                                                                                                                            |
| [**Иадскласс. Вспомогательная**](/windows/desktop/ADSI/iadsclass-property-methods)           | Указывает, является ли это вспомогательным классом.                                                                                                                                                                                                                                           |
| [**Иадскласс. Ауксдериведфром**](/windows/desktop/ADSI/iadsclass-property-methods)      | Массив вспомогательных классов, от которых наследует этот класс.                                                                                                                                                                                                                                     |
| [**Иадскласс. Container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Указывает, могут ли объекты этого класса содержать другие объекты, что имеет значение true, если любой класс включает этот класс в свой список **поссиблесупериорс**.                                                                                                                                 |
| [**Иадскласс. Дериведфром**](/windows/desktop/ADSI/iadsclass-property-methods)         | Массив классов, производным от которого является этот класс.                                                                                                                                                                                                                                       |
| [**Иадскласс. Мандаторипропертиес**](/windows/desktop/ADSI/iadsclass-property-methods) | Извлекает массив обязательных свойств, которые должны быть установлены для экземпляра класса. Возвращаемый список содержит все значения **mustContain** и **системмустконтаин** для класса и классов, от которых он производных, включая классы и вспомогательные классы. |
| [**Иадскласс. OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Возвращает governsID класса.                                                                                                                                                                                                                                                   |
| [**Иадскласс. OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | Извлекает массив необязательных свойств, которые могут быть установлены для экземпляра класса. Возвращаемый список содержит все значения **mayContain** и **системмайконтаин** для класса и классов, от которых он производных, включая классы и вспомогательные классы.   |
| [**Иадскласс. Поссиблесупериорс**](/windows/desktop/ADSI/iadsclass-property-methods)   | Извлекает массив значений **поссиблесупериорс** для класса, который указывает классы объектов, которые могут содержать объекты этого класса.                                                                                                                                        |



 

Абстрактная схема хранится в объекте **подсхемы** в контейнере схемы. Чтобы получить различающееся имя объекта **подсхемы** , выполните привязку к RootDSE и прочтите атрибут **субсчемасубентри** , как описано в разделе [Привязка без сервера и RootDSE](serverless-binding-and-rootdse.md). Имейте в виду, что более эффективно считывать абстрактную схему путем привязки к "LDAP://schema", чем путем привязки непосредственно к объекту **подсхемы** .

 

 
