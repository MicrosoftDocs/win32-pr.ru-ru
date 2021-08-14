---
description: Windows пользователи могут сохранять поиск в виде папки поиска, созданной XML-файлом, хранящим запрос в форме, которая может использоваться подсистемой поиска Windows.
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: Формат сохраненного файла поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 614eb357a82d2c70e068a9fa5258974423d755c48e779d5f5fe8be184a864d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863727"
---
# <a name="saved-search-file-format"></a>Формат сохраненного файла поиска

в Windows Vista и более поздних версиях пользователи могут сохранять поиск в виде папки поиска, созданной XML-файлом, хранящим запрос в форме, которая может использоваться подсистемой поиска Windows. В этом разделе описывается формат файла ( \* . Search-MS) и приведены следующие разделы.

- [Общие сведения о сохраненных поисковых запросах](#overview-of-saved-searches)
- [\<viewInfo> Элемент](/windows)
  - [\<viewInfo> Атрибута](/windows)
  - [\<viewInfo> Дочерние элементы](/windows)
- [\<query> Элемент](/windows)
  - [\<query> Дочерние элементы](/windows)
- [\<properties> Элемент](/windows)
- [Полная спецификация формата файла поиска MS](#full-specification-of-the-search-ms-file-format)
- [Примеры сохраненных поисков](#examples-of-saved-searches)

## <a name="overview-of-saved-searches"></a>Общие сведения о сохраненных поисковых запросах

пользователи могут сохранить поисковый запрос как папку поиска, виртуальную папку, отображаемую в Windows Explorer в папке "поиск". При открытии папки поиска выполняется сохраненный поиск и отображаются последние результаты. сохраненный файл поиска хранит запрос в формате, Windows может выполнять поиск, указывая, где искать, где искать, и как представлять результаты.

Сохраненный поиск создается из XML-файла ( \* . Search-MS) в папке поиска% UserProfile% \\ . Данные делятся на три первичных элемента в XML-файле:

- \<viewInfo> Указывает сведения о презентации
- \<query> Задает (Поиск сведений о запросе
- \<properties> Указывает свойства \* файла. Search-MS.

В следующем примере показана высокоуровневая структура сохраненного файла поиска.

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">

    <viewInfo ...>
        ...
    </viewInfo>

    <query>
        ...
    </query>

    <properties>
        ...
    </properties>

</persistedQuery>
```

## <a name="viewinfo-element"></a>Элемент \<viewInfo>

\<viewInfo>Элемент указывает, как результаты представляются конечному пользователю. В следующем примере показана структура элемента.

```XML
...
    <viewInfo viewMode=""
              iconSize=""
              stackIconSize=""
              autoListFlags=""
              folderFlags=""
              taskFlags=""
              displayName="">

        <visibleColumns>
            <column viewField=""/>
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/>
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>
        </columnChooserColumns >

        <groupBy viewField=""
                 direction=""/>

        <stackList>
            <stack viewField=""/>
        </stackList>

        <sortList>
            <sort viewField=""
                  direction=""/>
        </sortList>
    </viewInfo>
...
```

### <a name="viewinfo-attributes"></a>\<viewInfo> Атрибута

В таблице ниже описаны атрибуты элемента \<viewInfo>.

| attribute     | Описание                                                                     | Значения                     |
|---------------|---------------------------------------------------------------------------------|----------------------------|
| viewMode      | Указывает представление папки.                                                      | \|Плитки значков сведений \|  |
| iconSize      | Определяет размер значков и эскизов по умолчанию для элементов, если они не находятся в стеке. | Целое число от 16 до 256 |
| стаккиконсизе | Только для внутреннего использования. Не используйте.                                              | Недоступно                        |
| displayName   | Только для внутреннего использования. Не используйте.                                              | Недоступно                        |
| аутолистфлагс | Только для внутреннего использования. Не используйте.                                              | Недоступно                        |
| фолдерфлагс   | Только для внутреннего использования. Не используйте.                                              | Недоступно                        |
| таскфлагс     | Только для внутреннего использования. Не используйте.                                              | Недоступно                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> Дочерние элементы

дочерние элементы \<viewInfo> элемента указывают, какие столбцы отображаются в результатах поиска Windows Explorer и как группируются и сортируются результаты. Каждый дочерний элемент содержит упорядоченный набор столбцов, идентифицируемых каноническими именами системных свойств (например, System. DisplayName). Если он не определен в сохраненном файле поиска, то результаты поиска будут представлены с набором столбцов по умолчанию, подходящим для отображаемых типов файлов.

| Элемент               | Описание                                                                                        | Значения                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| висиблеколумнс        | Указывает упорядоченный список столбцов, отображаемых в представлении результатов. Пользователь может изменить этот список. | Любое системное свойство.                                         |
| фрекуентлюседколумнс | Только для внутреннего использования. Не используйте.                                                                 | Недоступно                                                          |
| колумнчусерколумнс  | Только для внутреннего использования. Не используйте.                                                                 | Недоступно                                                          |
| Применения               | Указывает одно системное свойство, по которому группируются результаты. Пользователь может изменить это значение.  | Любое системное свойство.                                         |
| сортлист              | Указывает упорядоченный список столбцов, по которым сортируются результаты.                                       | До четырех системных свойств. Пользователь может изменить этот список. |
| стакклист             | Только для внутреннего использования. Не используйте.                                                                 | Недоступно                                                          |

## <a name="query-element"></a>Элемент \<query>

\<query>Элемент задает атрибуты, определяющие, как запрашиваются результаты. В следующем примере показана структура элемента.

```XML
...
    <query>
        <providers>
            <provider clsid=""/>    <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

### <a name="query-child-elements"></a>\<query> Дочерние элементы

В таблице ниже описаны дочерние элементы элемента \<scope>.

| Элемент    | Описание                                                                                                               | Значение                                                                                                                                                                                                                                                          |
|------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| providers  | Только для внутреннего использования. Не используйте.                                                                                        | Недоступно                                                                                                                                                                                                                                                            |
| Вложенные запросы | Только для внутреннего использования. Не используйте.                                                                                        | Недоступно                                                                                                                                                                                                                                                            |
| Область      | Определяет расположения, которые нужно включить в поиск или исключить из него.                                                                 | Путь или [идентификатор известной папки](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) для включения или исключения. Этот элемент также может указывать, должен ли поиск включать или исключать дочерние пути (глубокий или глубокий поиск). |
| киндлист   | Определяет тип файлов для поиска.                                                                             | Любое значение System. Kind.                                                                                                                                                                                                                                         |
| условия | Задает правила фильтрации результатов. Например, результаты могут быть ограничены сообщениями электронной почты, отправленными или определенным пользователем. | andCondition, Оркондитион, Ноткондитион, Леафкондитион.                                                                                                                                                                                                        |

### <a name="scope-element"></a>Элемент \<scope>

\<scope>Элемент определяет расположения, которые необходимо включить в поиск или исключить из него. \<scope>Элемент должен содержать по крайней мере один \<include> дочерний элемент и ноль или более \<exclude> элементов. Расположения можно указать как путь (переменные среды поддерживаются) или как [идентификатор известной папки](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid). Кроме того, для каждого из этих расположений можно указать глубокий или поверхностный поиск, задав для нерекурсивного поиска значение true или false (по умолчанию рекурсия). Части включенного списка расположений можно исключить, указав элементы exclude.

Ниже показан \<scope> элемент, который будет искать в особой папке Documents, но не ее потомках, том "e:" и его дочерние элементы, но не каталог "e: \\ Windows" или любые его дочерние элементы:

```XML
...
    <query>
        ...
        <scope>
            <include knownFolder="{FDD39AD0-238F-46AF-ADB4-6C85480369C7}" nonRecursive="true"/>
            <include path="E:\"/>
            <exclude path="E:\Windows" nonRecursive="false"/>
        </scope>
        ...
    </query>
...
```

### <a name="kindlist-element"></a>Элемент \<kindList>

Эти элементы определяют объединение "вида" элементов, которые должны отображаться в библиотеке. Допустимые значения:

- календарь
- communication
- contact
- документ
- email
- feed
- folder
- игра
- инстантмессаже
- векселей
- link
- кинофильм
- music
- Примечание.
- picture
- программа
- рекордедтв
- сеарчфолдер
- задача
- видео
- Журнал
- item
- др.

### <a name="conditions-element"></a>Элемент \<conditions>

Условия — это фильтры, по которым сравниваются результаты поиска. Например, можно отфильтровать результаты, соответствующие определенным критериям, например имя автора или размер файла. Набор условий встроен в одно дерево условий с логическими и, или, а не ветвями.

В следующем примере показана структура \<condition> элемента.

```XML
...
    <query>
        ...
        <conditions>
            <condition type="" ...>
                <attributes>
                    <attribute attributeID="" .../>
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

Тип условия может быть одним из следующих:

| Тип          | Описание                                 | Доступные атрибуты                               |
|---------------|---------------------------------------------|----------------------------------------------------|
| andCondition  | Умножение двух или более дочерних условий | Недоступно                                                |
| оркондитион   | Отсоединение двух из более дочерних условий | Недоступно                                                |
| ноткондитион  | Отрицание дочернего условия               | Недоступно                                                |
| леафкондитион | Сравнивает свойство со значением                | свойство, propertyType, оператор, значение, ValueType |

\<leafCondition>Атрибуты элемента определяют свойства и значения, по которым фильтруются результаты.

### <a name="example-conditions-element"></a>Пример: \<conditions> элемент

В следующем примере отфильтруются результаты для всех непрочитанных элементов, созданных Джон. Это значит, что свойство System. «Read» имеет значение false, а строка «John» отображается в свойствах System. Author или System. Итемаусорс.

```XML
...
    <query>
        ...
        <conditions>

            <condition type="andCondition">

                <condition type="leafCondition"
                           property="System.IsRead"
                           operator="eq"
                           value="FALSE"/>

                <condition type="orCondition">

                    <condition type="leafCondition"
                               property="System.Author"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                    <condition type="leafCondition"
                               property="System.ItemAuthors"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                </condition>

            </condition>

        </conditions>

    </query>
...
```

## <a name="properties-element"></a>Элемент \<properties>

\<properties>Элемент описывает свойства сохраненного поиска. Сохраненные файлы поиска поддерживают четыре свойства: \<author> , \<kind> , \<description> и \<tags> . Они предназначены только для внутреннего использования.

## <a name="full-specification-of-the-search-ms-file-format"></a>Полная спецификация формата файла поиска MS

Ниже приведен пример полного XML-кода для сохраненного файла поиска.

```XML
<?xml version="1.0"?>

<persistedQuery version="1.0">

    <!-- The viewInfo section defines how results are displayed to the end user -->
    <viewInfo viewMode=""       <!-- details | icons | tiles -->
              iconSize=""       <!-- Integer -->
              stackIconSize=""  <!-- Do not use -->
              displayName=""    <!-- Do not use -->
              folderFlags=""    <!-- Do not use -->
              taskFlags=""      <!-- Do not use -->
              autoListFlags=""> <!-- Do not use -->

        <visibleColumns>
            <column viewField=""/>  <!-- System.[propertyname] -->
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/> <!-- Do not use -->
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>  <!-- Do not use -->
        </columnChooserColumns >

        <groupBy viewField=""       <!-- System.[propertyname] -->
                 direction=""/>     <!-- ascending | descending -->

        <stackList>
            <stack viewField=""/>   <!-- Do not use -->
        </stackList>

        <sortList>
            <sort viewField=""      <!-- System.[propertyname] -->
                  direction=""/>    <!-- ascending | descending -->
        </sortList>
    </viewInfo>

    <!-- The query section defines what gets searched (locations, file kinds) -->
    <query>
        <providers>
            <provider clsid=""/>          <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>

    <!-- The properties section identifies properties of the saved search file itself. -->
    <properties>
        ...             <!-- Do not use -->
    </properties>

</persistedQuery>
```

## <a name="examples-of-saved-searches"></a>Примеры сохраненных поисков

Ниже приведены примеры \* файлов. Search-MS.

### <a name="recent-documentssearch-ms"></a>Недавние документы. Поиск-МС

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUZZXD-30NU" propertyType="wstr" />
        </conditions>
        <kindList>
            <kind name="Document"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recent-musicsearch-ms"></a>Недавние музыкальные. Search — MS

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUW-1WNNU" propertyType="wstr"/>
        </conditions>
        <kindList>
            <kind name="Music"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recently-shared-by-mesearch-ms"></a>Недавно общие для меня. Поиск — МС

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <visibleColumns>
            <column viewField="System.ItemNameDisplay"/>
            <column viewField="System.DateModified"/>
            <column viewField="System.Keywords"/>
            <column viewField="System.SharedWith"/>
            <column viewField="System.ItemFolderPathDisplayNarrow"/>
        </visibleColumns>
        <frequentlyUsedColumns>
            <column viewField="System.Author"/>
            <column viewField="System.Kind"/>
            <column viewField="System.Size"/>
            <column viewField="System.Title"/>
            <column viewField="System.Rating"/>
        </frequentlyUsedColumns>
        <sortList>
            <sort viewField="System.SharedWith" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="andCondition">
                <condition type="leafCondition" property="System.IsShared" operator="eq" value="true"/>
                <condition type="leafCondition" property="System.FileOwner" operator="eq" value="[Me]"/>
            </condition>
        </conditions>
        <kindList>
            <kind name="item"/>
        </kindList>
        <scope>
            <include knownFolder="{5E6C858F-0E22-4760-9AFE-EA3317B67173}"/>
            <include knownFolder="{DFDF76A2-C82A-4D63-906A-5644AC457385}"/>
        </scope>
    </query>
</persistedQuery>
```
