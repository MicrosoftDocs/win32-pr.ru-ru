---
description: Запрос процесса в Windows Search
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Запрос процесса в Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3585f2cca2a6d5d8548a85ae8fac759ec94b4fa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117332"
---
# <a name="querying-process-in-windows-search"></a>Запрос процесса в Windows Search

Этот раздел организован следующим образом:

-   [О запросах в Windows Search](#about-querying-in-windows-search)
    -   [Локальные и удаленные запросы](#local-and-remote-queries)
    -   [Общие сведения об API структурированных запросов](#structured-query-api-overview)
-   [Сценарии запросов](#querying-scenarios)
    -   [Извлечение условий и синтаксический анализ запросов](#condition-extraction-and-query-parsing)
    -   [Запрос индекса](#querying-the-index)
-   [Связанные разделы](#related-topics)

## <a name="about-querying-in-windows-search"></a>О запросах в Windows Search

Запросы в Windows Search основаны на следующих четырех подходах:

-   [Расширенный синтаксис запросов](-search-3x-advancedquerysyntax.md) (АКС)
-   Синтаксис естественного запроса (НКС)
-   язык SQL
-   Интерфейсы структурированных запросов

АКС — это синтаксис запроса по умолчанию, используемый службой поиска Windows для запроса индекса и уточнения и сужения параметров поиска. АКС в основном используется для пользователя и может использоваться пользователями для создания запросов АКС, но может также использоваться разработчиками для программной сборки запросов. В Windows 7 был введен канонический АКС, который должен использоваться для программного создания запросов АКС. В Windows 7 и более поздних версиях параметр контекстного меню может быть доступен в зависимости от того, выполнено ли условие АКС. Дополнительные сведения см. в разделе «получение динамического поведения для статических команд с помощью расширенного синтаксиса запросов» раздела [Создание обработчиков контекстного меню](../shell/context-menu-handlers.md). Запросы АКС могут быть ограничены определенными типами файлов, которые называются типами файлов. Дополнительные сведения см. в разделе [типы файлов и ассоциации](../shell/fa-intro.md). Справочную документацию по соответствующим свойствам см. в разделе [System. Kind](../properties/props-system-kind.md)и [System. киндтекст](../properties/props-system-kindtext.md).

НКС — это синтаксис запроса, который является более ослабленным, чем АКС, и похож на естественный язык. НКС может использоваться службой поиска Windows для запроса индекса, если выбран параметр НКС, а не значение по умолчанию, АКС.

SQL — это язык текста, определяющий запросы. SQL является общим для различных технологий баз данных. Поиск Windows использует SQL, реализует его подмножество и расширяет его путем добавления элементов на язык. SQL Search для Windows расширяет стандартный синтаксис запросов к базе данных SQL-92 и SQL-99, что позволяет повысить его полезность при поиске на основе текста. Все функции SQL службы поиска Windows совместимы с Windows Search в Windows XP и Windows Server 2003 и более поздних версиях. Дополнительные сведения о SQL Search см. в разделе [запрос индекса с помощью синтаксиса SQL для поиска Windows](-search-sql-windowssearch-entry.md)и [обзор синтаксиса SQL Search](-search-sql-ovwofsearchquery.md).

Интерфейсы API структурированных запросов описаны далее в этом разделе. Справочную документацию по API-интерфейсам структурированных запросов см. в разделе [запросы интерфейсов](-search-querying-interfaces-entry-page.md). Такие интерфейсы, как [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , позволяют КОНСТРУИРОВАТЬ строки SQL из набора входных значений. Этот интерфейс преобразует запросы пользователей АКС в SQL Search в Windows и определяет ограничения запросов, которые могут быть выражены в SQL, но не в АКС. [**Исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) также получает строку подключения OLE DB для подключения к базе данных Windows Search.

### <a name="local-and-remote-queries"></a>Локальные и удаленные запросы

Запросы можно выполнять как локально, так и удаленно. В следующем примере показан локальный запрос с [предложением from](-search-sql-from.md) . Локальный запрос запрашивает только локальный каталог Системиндекс.


```
FROM SystemIndex
```



В следующем примере показан удаленный запрос с [предложением from](-search-sql-from.md) . Добавление ComputerName преобразует предыдущий пример в удаленный запрос.


```
FROM [<ComputerName>.]SystemIndex
```



По умолчанию в Windows XP и Windows Server 2003 не установлен Windows Search. Только Windows Search 4 (WS4) предоставляет поддержку удаленного запроса. Предыдущие версии Windows Desktop Search (WDS), например 3,01 и более ранних версий, не поддерживают удаленный запрос. С помощью проводника Windows можно запрашивать локальный индекс удаленного компьютера для элементов файловой системы (элементы, обрабатываемые протоколом file:).

Чтобы получить элемент по удаленному запросу, элемент должен удовлетворять следующим требованиям.

-   Быть доступным через UNC-путь.
-   Существует на удаленном компьютере, к которому имеет доступ клиент.
-   Имеет свой набор безопасности, позволяющий клиенту иметь доступ на чтение.

В проводнике Windows есть функции для совместного использования элементов, включая общедоступный общий ресурс (общедоступный \\ \\ компьютер \\ \\ ...) в **центре управления сетями и общим доступом**, а также общий ресурс пользователей ( \\ \\ \\ пользователей компьютеров.. \\ .) для элементов, общих через мастер общего доступа. После предоставления общего доступа к папкам можно запросить локальный индекс, указав имя компьютера удаленного компьютера в предложении FROM, и UNC-путь на удаленном компьютере в предложении SCOPE. В следующем примере показан удаленный запрос, использующий предложения FROM и SCOPE.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



В приведенных здесь примерах используется SQL.

### <a name="structured-query-api-overview"></a>Общие сведения об API структурированных запросов

Структурированный запрос предоставляет возможность поиска информации по логическим комбинациям запросов по отдельным свойствам. В этом разделе описаны функциональные возможности наиболее важных интерфейсов API и методов структурированных запросов. Справочную документацию по API-интерфейсам структурированных запросов см. в разделе [запросы интерфейсов](-search-querying-interfaces-entry-page.md).

### <a name="iqueryparser"></a>икуерипарсер

Метод [**икуерипарсер::P Арсе**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) анализирует входную строку пользователя и формирует интерпретацию в форме [**икуерисолутион**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution). Если параметр *пкустомпропертиес* этого метода не равен null, то это перечисление объектов [**ириччунк**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) (по одному для каждого распознанного пользовательского свойства). Другие методы [**икуерипарсер**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) позволяют приложению задавать несколько параметров, таких как языковой стандарт, схема, средство разбиения по словам и обработчики для различных типов именованных сущностей. [**Икуерипарсер:: жетсчемапровидер**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) возвращает интерфейс [**исчемапровидер**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) для обзора загруженной схемы.

### <a name="iquerysolution--iconditionfactory"></a>Икуерисолутион: Икондитионфактори

Интерфейс [**икуерисолутион**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) предоставляет всю информацию о результатах синтаксического анализа входной строки. Так как **икуерисолутион** также является интерфейсом [**икондитионфактори**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) , можно создавать дополнительные узлы дерева условий. Метод [**икуерисолутион::-Query**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) создает дерево условий для интерпретации. **Икуерисолутион::** также возвращает семантический тип.

### <a name="iconditionfactory"></a>икондитионфактори

[**Икондитионфактори**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) создает узлы дерева условий. Если параметр *упрощения* [**Икондитионфактори:: Макенот**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) имеет значение **Variant \_ true**, то результирующий [**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) упрощен и не должен быть узлом отрицания. Если параметр *псубкондитионс* параметра [**Икондитионфактори:: макеандор**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) не равен null, то этот параметр должен быть перечислением объектов [**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) и стать поддеревьями. [**Икондитионфактори:: макелеаф**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) конструирует конечный узел с указанным именем свойства, операцией и значением. Строка в параметре *пвалуетипе* должна быть именем семантического типа из схемы. Если параметр *expand* имеет значение **Variant \_ true** и свойство является виртуальным, то результирующее дерево условий обычно является отсоединением, полученным от расширения свойства до определенных составляющих. Если значение не равно null, параметры *ппропертинаметерм*, *поператортерм* и *пвалуетерм* должны обозначать термины, указывающие свойство, операцию и значение.

### <a name="icondition--ipersiststream"></a>Икондитион: IPersistStream

Интерфейс [**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) — это отдельный узел в дереве условий. Узел может быть узлом отрицания, узлом, узлом или конечным узлом. Для неоконечного узла [**икондитион:: жетсубкондитионс**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) возвращает перечисление поддеревьев. Для конечного узла следующие методы [**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) возвращают следующие значения:

-   [**Жеткомпарисонинфо**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) возвращает имя свойства, операцию и значение.
-   Функция [**ValueType**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) возвращает семантический тип значения, который был спеЦифиЦиед в параметре *псзвалуетипе* объекта [**икондитионфактори:: макелеаф**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf).
-   [**Жетвалуенормализатион**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) возвращает строковый формат значения. (Если значение было уже строкой, эта форма будет нормализована в зависимости от регистра, диакритических знаков и т. д.).
-   [**Жетинпуттермс**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) возвращает сведения о том, какие части входного предложения создали имя свойства, операцию и значение.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) Возвращает глубокую копию дерева условий.

### <a name="irichchunk"></a>ириччунк

Каждый объект [**ириччунк**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) определяет диапазон токена и строку. **Ириччунк** — это служебный интерфейс, который представляет сведения о диапазоне (обычно это диапазон токенов), определяемый начальной позицией и длиной. Эти сведения о диапазоне включают строку и (или) **вариант**.

### <a name="iconditiongenerator"></a>икондитионженератор

Интерфейс [**икондитионженератор**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) предоставляется приложением для управления созданием дерева условий распознавания и условия для именованного типа сущности. Генератор условий передается [**икуерипарсер**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) через [**Икуерипарсер:: сетмултиоптион**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption). [**Икуерипарсер**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) вызывает [**Икондитионженератор:: Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) с [**исчемапровидер**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) для текущей загруженной схемы. Это позволяет [**икондитионженератор**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) получить все необходимые сведения о схеме. При синтаксическом анализе входной строки **икуерипарсер** вызывает метод [**Икондитионженератор:: рекогнизенамедентитиес**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) каждого [**икондитионженератор**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), чтобы можно было сообщить о возникновении именованных сущностей, распознаваемых во входной строке. **Икуерипарсер** может использовать текущий языковой стандарт и использовать разметку входных данных, так как они должны сообщать о диапазонах маркеров любых именованных сущностей.

Когда [**икуерипарсер**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) собирается выдать конечный узел, а семантический тип значения соответствует именованному типу сущности для [**икондитионженератор**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), **Икуерипарсер** вызывает [**икондитионженератор:: женератефорлеаф**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) со сведениями для создаваемого узла. Если [**икондитионженератор**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) возвращает " \_ ОК", он должен возвращать дерево условий (которое не обязательно должно быть конечным узлом) и информировать **икуерипарсер** , следует ли подавлять альтернативную интерпретацию строки, которая обычно создается в качестве меры предосторожности.

### <a name="itokencollection"></a>итокенколлектион

Метод [**итокенколлектион:: нумберофтокенс**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) возвращает число токенов. [**Итокенколлектион::-Token**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) возвращает сведения о *i*-ом маркере. Начало и длина являются позициями символов во входной строке. Возвращаемый текст будет иметь значение, отличное от NULL, только если имеется текст, переопределяющий символы из входной строки. Это используется, например, для переопределения тире во входной строке, если этот дефис находится в контексте, где его следует интерпретировать как отрицание.

### <a name="inamedentitycollector"></a>инамедентитиколлектор

[**Икондитионженератор**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) вызывает [**Инамедентитиколлектор:: Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) для каждой распознанной известной сущности. Диапазоны — это диапазоны маркеров. Это всегда должно быть так, как *бегинспан* ? *бегинактуал*  <  *ендактуал* ? *ендспан*. *бегинспан* и *ендспан* могут отличаться от *бегинактуал* и *ендактуал* , если именованная сущность начинается и (или) заканчивается на семантически незначимых маркерах, таких как кавычки (которые, тем не менее, покрываемые именованной сущностью). Значение должно быть выражено в виде строки и впоследствии появиться в вызове [**икондитионженератор:: женератефорлеаф**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf).

### <a name="ischemaprovider"></a>исчемапровидер

Интерфейс [**исчемапровидер**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) можно использовать для просмотра загруженной схемы для сущностей (типов) и связей (свойств). Вот как это делают отдельные методы:

-   [**Сущности**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) возвращают перечисление всех сущностей ([**иентити**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) в схеме.
-   [**Рутентити**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) Возвращает корневую сущность схемы. Для плоской схемы возвращается основной тип каждого [**икуерисолутион**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) .
-   [](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) Функция GetSchema находит сущность по имени и возвращает \_ значение S false, если такая сущность отсутствует в схеме.
-   [**Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) возвращает перечисление интерфейсов [**иметадата**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) .

### <a name="ientity"></a>иентити

Интерфейс [**иентити**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) — это сущность схемы, которая представляет тип с именем, имеет ряд именованных связей с другими типами (свойства) и является производным от базовой сущности. Вот что делают отдельные методы:

-   [**Иентити:: Relationships**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) возвращает перечисление объектов [**ирелатионшип**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) , по одному для каждого исходящего отношения этого типа. Каждое исходящее отношение сущности имеет имя.
-   [**Иентити::-relationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) находит связь по имени и возвращает \_ значение S false, если такая связь для этой сущности отсутствует.
-   [**Иентити:: Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) возвращает перечисление интерфейсов [**иметадата**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , по одному для каждой пары метаданных этой сущности.
-   [**Иентити::D ефаултфрасе**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) возвращает фразу по умолчанию для упрощения создания АКС или нксго состояния дерева условий.

### <a name="irelationship"></a>ирелатионшип

Интерфейс [**ирелатионшип**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) представляет связь между двумя сущностями: источником и назначением. Вот как это делают отдельные методы:

-   [**Ирелатионшип:: Real**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) сообщает, является ли связь реальной. Например, если сущность A является производной от сущности B и наследует связь с именем R от нее, то может по-прежнему иметь собственную связь с именем R. Однако связь, Бевин и R, должна иметь тот же конечный тип, что и в B, и единственная причина для ее существования — хранить метаданные, относящиеся к B. Такая связь с B считается недействительной.
-   [**Ирелатионшип:: метаданным**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) возвращает перечисление интерфейсов [**иметадата**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , по одному для каждой пары метаданных этой сущности.
-   [**Ирелатионшип::D ефаултфрасе**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) возвращает фразу по умолчанию, используемую для этой связи в передействиях. Каждая связь имеет фразу по умолчанию, которая обозначает, что она позволяет упростить создание АКС или НКСного состояния дерева условий.

### <a name="imetadata"></a>иметадата

Метаданные представляют собой пары "ключ-значение", каждый из которых связан с сущностью, связью или всей схемой. Поскольку ключи не обязательно являются уникальными, коллекция метаданных может рассматриваться как несколько карт. Метод [**иметадата:: GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) вызывается для получения ключа и значения для пары отражение.

## <a name="querying-scenarios"></a>Сценарии запросов

В следующих сценариях описывается использование интерфейсов API структурированных запросов в Windows Search в общих сценариях запросов, таких как создание дерева условий и запрос индекса.

### <a name="condition-extraction-and-query-parsing"></a>Извлечение условий и синтаксический анализ запросов

При создании запроса его область определяется путем указания системы на место поиска. Это ограничит результаты поиска. После определения области применяется фильтр, и возвращается набор фильтров. Результаты поиска ограничиваются путем построения дерева условий с конечными узлами аналогично графу. Затем эти условия извлекаются. Дерево условий — это логическое сочетание (и, или, не) конечных условий, каждое из которых связывает свойство с помощью операции со значением. Конечный узел представляет ограничение для одного свойства на значение через некоторые операции.

Для ограничения фильтра требуется логическое выражение, описывающее это ограничение. Определение этого выражения начинается с интерфейса [**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) , который используется для создания одного узла в дереве условий. Поскольку в следующем примере присутствует только одно условие, дерево не изменяется.


```C++
    
    [
        object,
        uuid(0FC988D4-C935-4b97-A973-46282EA175C8),
        pointer_default(unique)
    ]
    interface ICondition : IPersistStream
    {
        HRESULT GetConditionType([out, retval] CONDITION_TYPE* pNodeType);
        HRESULT GetSubConditions([in] REFIID riid, [out, retval, iid_is(riid)] void** ppv);
        [local] HRESULT GetComparisonInfo([out, annotation("__deref_opt_out")] LPWSTR *ppszPropertyName, [out, annotation("__out_opt")] CONDITION_OPERATION *pOperation, [out, annotation("__out_opt")] PROPVARIANT *pValue);
        HRESULT GetValueType([out, retval] LPWSTR* ppszValueTypeName);
        HRESULT GetValueNormalization([out, retval] LPWSTR* ppszNormalization);
        [local] HRESULT GetInputTerms([out, annotation("__out_opt")] IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] IRichChunk** ppValueTerm);
        HRESULT Clone([out, retval] ICondition** ppc);
    };


```



Если имеется более одного условия фильтра, то для достижения одного дерева используются и другие логические операторы. И-деревья и-деревья представляют собой соединения и пересечения их поддеревьев. Недерево представляет отрицание отдельного поддерева. АКС предоставляет текстовый подход к достижению логических выражений с логическими операторами, и зачастую проще.

В следующем примере мы преобразуем дерево условий ([**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) в визуальную форму. Средство синтаксического анализа запросов, использующее интерфейс [**икуерипарсер**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) , преобразует [**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) в строку запроса форматированного текста (RTF). Метод [**икуерипарсер:: рестатетостринг**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) возвращает текст запроса, а метод [**икуерипарсер::P Арсе**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) создает интерфейс [**икуерисолутион**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) . В следующем примере показано, как выполнить все эти действия.


```C++
    [
        object,
        uuid(2EBDEE67-3505-43f8-9946-EA44ABC8E5B0),
        pointer_default(unique)
    ]
    interface IQueryParser : IUnknown
    {
        HRESULT Parse([in] LPCWSTR pszInputString, [in] IEnumUnknown* pCustomProperties, [out, retval] IQuerySolution** ppSolution);
        HRESULT SetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [out, retval] PROPVARIANT* pOptionValue);
        HRESULT SetMultiOption([in] STRUCTURED_QUERY_MULTIOPTION option, [in] LPCWSTR pszOptionKey, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetSchemaProvider([out, retval] ISchemaProvider** ppSchemaProvider);
        HRESULT RestateToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszQueryString);
        HRESULT ParsePropertyValue([in] LPCWSTR pszPropertyName, [in] LPCWSTR pszInputString, [out, retval] IQuerySolution** ppSolution);
        HRESULT RestatePropertyValueToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszPropertyName, [out] LPWSTR* ppszQueryString);
    };

```



Основной вход для [**икуерипарсер::P Арсе**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) — это входная пользовательская строка, которую необходимо проанализировать, но приложение также может сообщать анализатору запросов все свойства, распознаваемые во входных данных (из синтаксиса конкретного приложения). Выходные данные **икуерипарсер::P Арсе** — это [**икуерисолутион**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution), который предоставляет всю информацию, относящуюся к этому вызову синтаксического анализа. Существуют методы для получения входной строки, способа разметки входной строки, любых ошибок синтаксического анализа и проанализированного запроса в качестве дерева условий, представленного [**икондитион**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition). В следующем примере показано...


```C++
    [
        object,
        uuid(D6EBC66B-8921-4193-AFDD-A1789FB7FF57),
        pointer_default(unique)
    ]
    interface IQuerySolution : IConditionFactory
    {
        [local] HRESULT GetQuery([out, annotation("__out_opt")] ICondition** ppQueryNode, [out, annotation("__out_opt")] IEntity** ppMainType);
        HRESULT GetErrors([in] REFIID riid, [out, retval, iid_is(riid)] void** ppParseErrors);
        [local] HRESULT GetLexicalData([out, annotation("__deref_opt_out")] LPWSTR* ppszInputString, [out, annotation("__out_opt")] ITokenCollection** ppTokens, [out, annotation("__out_opt")] LCID* pLocale, [out, annotation("__out_opt")] IUnknown** ppWordBreaker);
    }    

    

```



В предыдущем примере [**икуерисолутион::**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) gettext может получить любые сведения о запросе, включая исходный текст, токены, составляющие текст, или дерево условий. Примеры возможных значений запроса перечислены в следующей таблице.



| Примеры возвращаемых значений запроса                        | Описание                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | Текст запроса, [**икуерипарсер:: рестатетостринг**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) , возвращает |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | Разбиение маркеров                                                                                  |
| ![неразрешенное дерево условий](images/queryvalues1.png) | Неразрешенное дерево условий                                                                              |



 

Возвращенное начальное дерево условий не разрешено. В неразрешенном дереве условий ссылки на дату и время, такие как `date:yesterday` , не преобразуются в абсолютное время. Кроме того, виртуальные свойства не разворачиваются. Виртуальные свойства — это свойства, которые действуют как статистические выражения нескольких свойств.

Например, запрос `kind:email from:reljai` создает следующие неразрешенные и разрешенные деревья условий. Неразрешенное дерево условий — слева, а разрешенное дерево условий — справа.

![деревья неразрешенных и разрешенных условий](images/conditiontree.png)

Разрешенное дерево можно получить путем вызова [**икондитионфактори:: Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve). Однако передача [**скро \_ не с \_ разрешением \_ DateTime**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) оставляет дату и время неразрешимыми. Неразрешенное дерево условий имеет свои преимущества, так как неразрешенное дерево условий содержит сведения о запросе. Каждый конечный узел указывает на маркеры, возвращаемые [**икуерисолутион:: жетлексикалдата**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata), которые соответствуют свойству, оператору и значению при использовании интерфейса [**ириччунк**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) . В следующем примере показано...


```C++
    interface ITokenCollection : IUnknown
    {
        HRESULT NumberOfTokens(ULONG* pCount);
        HRESULT GetToken([in] ULONG i, [out, annotation("__out_opt")] ULONG* pBegin, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz);
    };

ICondition:: GetInputTerms([out, annotation("__out_opt")] 
IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] 
IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] 
IRichChunk** ppValueTerm);

    interface IRichChunk : IUnknown
    {
        HRESULT GetData([out, annotation("__out_opt")] ULONG* pFirstPos, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz, [out, annotation("__out_opt")] PROPVARIANT* pValue);
    }
```



### <a name="querying-the-index"></a>Запрос индекса

Существует несколько подходов к отзапросу индекса. Некоторые из них основаны на SQL, а другие — на АКС. Индекс службы поиска Windows можно также запрашивать программно с помощью [интерфейсов запросов](./-search-querying-interfaces-entry-page.md). Существует три интерфейса, которые относятся к запросам индекса: [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), [**ировсетприоритизатион**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)и [**ировсетевентс**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Основные сведения см. [в разделе Запрос индекса программным способом](-search-3x-wds-qryidx-overview.md).

Можно разработать компонент или вспомогательный класс для запроса индекса с помощью интерфейса [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . Этот интерфейс реализуется как вспомогательный класс для [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (и [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) и получается путем вызова [**исеарчкаталогманажер:: жеткуерихелпер**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Основные сведения см. [в разделе запросы к индексу с помощью исеарчкуерихелпер](-search-3x-wds-qryidx-searchqueryhelper.md).

[**Исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) позволяет:

-   Получите строку подключения OLE DB для подключения к базе данных Windows Search.
-   Преобразование запросов пользователя АКС в SQL Search в Windows.
-   Укажите ограничения запросов, которые могут быть выражены в SQL, но не в АКС.

Приоритеты индексирования и события наборов строк поддерживаются в Windows 7 и более поздних версиях. В [**ировсетприоритизатион**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) есть стек приоритетов, который позволяет клиенту запрашивать, что области, используемые в определенном запросе, должны иметь более высокий приоритет. [**Ировсетевентс**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) предоставляет уведомления об изменениях элементов в наборах строк, включая добавление новых элементов, удаление элементов и изменение данных элемента. Использование уведомлений о событиях наборов строк гарантирует, что результаты для существующих запросов будут как можно более актуальными. Основные сведения см. [в разделе индексирование определения приоритетов и событий набора строк в Windows 7](indexing-prioritization-and-rowset-events.md).

## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[Индексирование, запросы и уведомления в Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Что включено в индекс](-search-indexing-process-overview.md)
</dt> <dt>

[Процесс индексирования в Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Обработка уведомлений в Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Требования к форматированию URL-адресов](url-formatting-requirements.md)
</dt> </dl>

 

 
