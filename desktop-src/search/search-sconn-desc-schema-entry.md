---
description: представляет схему описания соединителя поиска, используемую библиотеками Windows Explorer и федеративными поставщиками поиска.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Схема описания соединителя поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8d8ab60ba472cca961a4208b1c551679ef93eacd46e07cf5e080a3e73f3d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226385"
---
# <a name="search-connector-description-schema"></a>Схема описания соединителя поиска

представляет схему описания соединителя поиска, используемую библиотеками Windows Explorer и федеративными поставщиками поиска. Схема определяет структуру и требования для файлов описания соединителя поиска ( \* . сеарчконнектор-MS) и **сеарчконнектордескриптионтипе** элементов в файлах описания библиотеки оболочки ( \* . Library-MS).

В этом разделе описывается схема, связанная с соединителями федеративного поиска. Дополнительные сведения о библиотеках и схеме описания библиотеки см. в разделе [Библиотека описание схемы](../shell/library-schema-entry.md).

Этот раздел включает следующие подразделы:

-   [Что такое соединители поиска?](#what-are-search-connectors)
-   [Как работают файлы описания соединителя поиска?](#search-connector-description-schema)
-   [Что такое схема описания соединителя поиска?](#what-is-the-search-connector-description-schema)
-   [Каковы основные части схемы?](#what-are-the-major-parts-of-the-schema)
-   [Примеры файлов описания соединителя поиска](#examples-of-search-connector-description-files)
-   [Дополнительные ресурсы](#additional-resources)
-   [Связанные темы](#related-topics)

## <a name="what-are-search-connectors"></a>Что такое соединители поиска?

Соединители поиска соединяют пользователей с данными, хранящимися в веб-службах или в расположениях удаленного хранилища. с Windows 7 пользователи могут устанавливать соединители поиска для таких расположений, как веб-службы, чтобы они могли искать данные в этих расположениях непосредственно из обозревателя Windows. Соединители поиска — это файлы описания соединителя поиска ( \* . сеарчконнектор-MS), которые определяют способ подключения к, отправки запросов и получения результатов из расположения.

Помимо веб-служб, соединители поиска можно использовать для поиска областей локальных индексов, созданных обработчиками протоколов. Например, пользователи могут искать электронное письмо по электронной почте с помощью обработчика протокола MAPI, используя соединитель поиска для этого хранилища электронной почты.

## <a name="how-do-search-connector-description-files-work"></a>Как работают файлы описания соединителя поиска?

когда файлы описания соединителя поиска устанавливаются в системах пользователей, пользователи могут открыть обозреватель Windows, щелкнуть соединитель поиска в области навигации и ввести поисковый запрос. Windows Обозреватель отправляет запрос, используя сведения из файла описания соединителя поиска, например используемый поставщик и область поиска. Результаты возвращаются в виде элементов канала RSS или Atom и отображаются пользователям как обычные элементы оболочки.

Развертывание файла описания соединителя поиска зависит от типа расположения, поддерживаемого соединителем поиска.

-   в файле конфигурации OpenSearch ( \* . osdx-) для веб-службы
-   В рамках установки обработчика протокола

При открытии файла OSDX-или установке обработчика протокола необходимо убедиться, что выполняются следующие действия.

-   файл. сеарчконнектор-ms создается в папке "Windows" пользователем " **поиск** " (% userprofile%/сеарчес).
-   Ярлык для файла. сеарчконнектор-MS создается в папке " **Links** " пользователей (% UserProfile%/Линкс).

## <a name="what-is-the-search-connector-description-schema"></a>Что такое схема описания соединителя поиска?

Схема описания соединителя поиска — это схема XML, которая определяет структуру файлов описания соединителя поиска ( \* . сеарчконнектор-MS). Каждый соединитель поиска должен иметь файл описания соединителя поиска, указывающий способ подключения к, отправки запросов и получения результатов из расположения.

## <a name="what-are-the-major-parts-of-the-schema"></a>Каковы основные части схемы?

В следующей таблице перечислены основные части схемы.



| Дочерние элементы                                                                         | Описание                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [иссеарчонлитем](search-schema-sconn-issearchonlyitem.md)                           | Определяет, поддерживаются ли в соединителе поиска расположения только для поиска или поиска и просмотра.                                                                                |
| [исдефаултсавелокатион](search-schema-sconn-isdefaultsavelocation.md)                 | Только для использования в библиотеке.                                                                                                                                                                   |
| [исдефаултноновнерсавелокатион](search-schema-sconn-isdefaultnonownersavelocation.md) | Только для использования в библиотеке.                                                                                                                                                                   |
| [description](search-schema-sconn-description.md)                                     | Описывает соединитель поиска.                                                                                                                                                         |
| [иконреференце](search-schema-sconn-iconreference.md)                                 | Определяет расположение пользовательского значка для соединителя поиска.                                                                                                                      |
| [имажелинк](search-schema-sconn-imagelink.md)                                         | Определяет расположение пользовательского эскиза для соединителя поиска.                                                                                                                 |
| [календаря](search-schema-sconn-author.md)                                               | Определяет автора соединителя поиска.                                                                                                                                          |
| [dateCreated](search-schema-sconn-datecreated.md)                                     | Определяет дату создания соединителя поиска.                                                                                                                              |
| [темплатеинфо](search-schema-sconn-templateinfo.md)                                   | Указывает тип папки для соединителя поиска.                                                                                                                                       |
| [локатионпровидер](search-schema-sconn-locationprovider.md)                           | Указывает поставщика поиска для использования этим соединителем поиска.                                                                                                                      |
| [область](search-schema-sconn-scope.md)                                                 | Задает расположения для включения в область поиска и исключения из нее.                                                                                                                |
| [пропертисторе](search-schema-sconn-propertystore.md)                                 | Указывает расположение [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) на основе XML для этого соединителя поиска. **Ипропертисторе** поддерживает открытые метаданные соединителя поиска. |
| [инклудеинстартменускопе](search-schema-sconn-includeinstartmenuscope.md)             | указывает, следует ли включать в область поиска меню расположение, представленное соединителем поиска.                                                                 |
| [поддомен](search-schema-sconn-domain.md)                                               | Определяет домен верхнего уровня соединителя поиска.                                                                                                                                     |
| [суппортсадванцедкуерисинтакс](search-schema-sconn-supportsadvancedquerysyntax.md)     | Указывает, поддерживает ли соединитель поиска расширенный синтаксис запросов (АКС).                                                                                                            |
| [Индексируется](search-schema-sconn-isindexed.md)                                         | Указывает, индексировано ли расположение, представленное соединителем поиска.                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>Примеры файлов описания соединителя поиска

Ниже приведен пример файла описания соединителя поиска для федеративной веб-службы поиска.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



Ниже приведен пример файла описания соединителя поиска для обработчика протокола MAPI.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a>Дополнительные ресурсы

-   Дополнительные сведения о схеме описания библиотеки см. в разделе [Библиотека описание схемы](../shell/library-schema-entry.md).
-   Дополнительные сведения об установке соединителя поиска см. в разделе [федеративный поиск в Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)](search-schema-searchconnectordescription.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[OpenSearch](http://www.opensearch.org/Home)
</dt> <dt>

[Центре загрузки Майкрософт](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
