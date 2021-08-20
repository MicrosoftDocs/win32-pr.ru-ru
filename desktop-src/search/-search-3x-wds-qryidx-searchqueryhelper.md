---
description: 'Для запроса индекса можно использовать интерфейс Исеарчкуерихелпер. Этот интерфейс реализуется как вспомогательный класс для Исеарчкаталогманажер (и ISearchCatalogManager2) и получается путем вызова Исеарчкаталогманажер:: Жеткуерихелпер.'
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Запрос индекса с помощью Исеарчкуерихелпер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db9bf2fe8d593d95a1a8f58e25faebb4b76a65ac28fe4c1bc6d6dc2f25ab87d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052106"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a>Запрос индекса с помощью Исеарчкуерихелпер

Для запроса индекса можно использовать интерфейс [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . Этот интерфейс реализуется как вспомогательный класс для [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (и [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) и получается путем вызова [**исеарчкаталогманажер:: жеткуерихелпер**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Этот интерфейс позволяет выполнять следующие задачи:

-   получите строку подключения OLE DB для подключения к Windows базе данных поиска.
-   преобразуйте запросы пользователей расширенного синтаксиса запросов (акс) в Windows язык SQL поиска (SQL).
-   укажите ограничения запроса, которые могут быть выражены в SQL, но не в акс.

Этот раздел организован следующим образом:

-   [начало работы с Исеарчкуерихелпер](#getting-started-with-isearchqueryhelper)
-   [Использование метода Женератесклфромусеркуери](#using-the-generatesqlfromuserquery-method)
-   [Работа с идентификаторами языковых стандартов](#working-with-locale-identifiers)
-   [Работа со свойствами и столбцами](#working-with-properties-and-columns)
-   [Работа с расширением термина запроса](#working-with-query-term-expansion)
-   [Работа с другими методами Исеарчкуерихелпер](#working-with-other-isearchqueryhelper-methods)
-   [Связанные темы](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a>начало работы с Исеарчкуерихелпер

существует несколько ключевых интерфейсов и методов, о которых следует знать, прежде чем можно будет запустить программный запрос Windows поиска с помощью интерфейса [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . На высоком уровне необходимо выполнить следующие действия.

1.  Создайте экземпляр [**исеарчманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  Получите экземпляр [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) с помощью [**Исеарчманажер:: catalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog). имя системного каталога для Windows поиска: `SYSTEMINDEX` .
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  Получите экземпляр [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) с помощью [**Исеарчкаталогманажер:: жеткуерихелпер**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper).
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  после создания экземпляра [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)можно получить строку подключения, используемую для подключения к соединителю OLE DB индекса поиска Windows.
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a>Использование метода Женератесклфромусеркуери

метод [**исеарчкуерихелпер:: женератесклфромусеркуери**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) преобразует входные данные пользователя в строку запроса SQL, которую затем можно отправить поставщику OLE DB для Windows поиска. этот метод преобразует запрос [синтаксиса расширенных запросов](-search-3x-advancedquerysyntax.md) (акс) или синтаксиса естественного запроса (нкс), введенный пользователем в SQL, и позволяет добавлять другие фрагменты SQL по мере необходимости.

строка запроса SQL возвращается в следующей форме:


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



ниже приведен пример строки SQL, возвращаемой из вызова `GenerateSQLFromUserQuery("comput")` :


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> Метод создает предикаты FREETEXT и CONTAINS, поскольку содержит только один из них не создает осмысленный ранг.

 

## <a name="working-with-locale-identifiers"></a>Работа с идентификаторами языковых стандартов



| Метод                                                                                                                                                                                                                                   | Описание                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Исеарчкуерихелпер:: Get \_ куериконтентлокале**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/<br/> [**Исеарчкуерихелпер::p UT \_ куериконтентлокале**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | Возвращает или задает код языка (LCID) запроса. Это помогает получить правильное средство разбиения на слова и парадигматические модули для сравнения терминов запроса с каталогом или инвертированным индексом. По умолчанию используется текущий языковой стандарт ввода. |
| [**Исеарчкуерихелпер:: Get \_ куерикэйвордлокале**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/<br/> [**Исеарчкуерихелпер::p UT \_ куерикэйвордлокале**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | Возвращает или задает LCID для языка, используемого при синтаксическом анализе ключевых слов синтаксиса расширенных запросов (АКС). По умолчанию используется языковой стандарт пользователя по умолчанию.                                                                              |



 

Языковой стандарт **содержимого** и **ключевое слово locale** являются идентификаторами языкового стандарта (LCID), которые помогают поисковой подсистеме использовать правильные средства разбиения по словам, определяя язык терминов запроса и ключевые слова языка АКС. они не всегда являются одинаковыми lcid, так как Windows поиск предоставляется в нескольких международных версиях, а также включает пакеты многоязычный пользовательский интерфейс (MUI) для других языков. Языковой стандарт содержимого определяет код языка, на котором пользователи выполняют поисковый запрос в, а язык ключевых слов определяет код языка, используемый поисковой системой при анализе ключевых слов синтаксиса расширенных запросов (АКС).

Например, при наличии английской версии (без пакетов MUI) языковой стандарт содержимого и ключевое слово keyword имеют значение 1033. Если у вас установлена немецкая версия без пакетов MUI, то языковой стандарт содержимого и ключевое слово locale имеют значение 1031 (GR-GR). Однако если у вас установлена английская версия с пакетом MUI для румынского языка, то язык содержимого — 2072 (ro), а ключевое слово locale — 1033 (EN-US).

## <a name="working-with-properties-and-columns"></a>Работа со свойствами и столбцами



| Методы                                                                                                                                                                                                                                                  | Описание                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Исеарчкуерихелпер:: Get \_ куериконтентпропертиес**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/<br/> [**Исеарчкуерихелпер::p UT \_ куериконтентпропертиес**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | Возвращает или задает свойства содержимого для поиска (столбец свойств, указанный в предложениях CONTAINS или FREETEXT).                                   |
| [**Исеарчкуерихелпер:: Get \_ куериселектколумнс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/<br/> [**Исеарчкуерихелпер::p UT \_ куериселектколумнс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | Возвращает или задает столбцы (или свойства), запрошенные в инструкции SELECT. Значение по умолчанию — System. Итемурл и свойства, используемые в предложении WHERE. |



 

Элементы представлены в хранилище свойств в виде строки. Каждая строка содержит ряд столбцов, представляющих свойства этого элемента. Не все элементы будут иметь значение для заданного свойства. Например, звуковой файл обычно не содержит значение свойства System. Property. Фромнаме, но может содержать сведения о System. Music. исполнителя.

С помощью этих методов вы получите доступ к свойству или измените его с помощью строки в Юникоде с разделителями-запятыми, заканчивающейся нулем, которая указывает одно или несколько имен столбцов в хранилище свойств: "System.Docумент. Автор, System.Docумент. Title ".

## <a name="working-with-query-term-expansion"></a>Работа с расширением термина запроса



| Методы                                                                                                                                                                                                                                 | Описание                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [**Исеарчкуерихелпер:: Get \_ куеритермекспансион**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [**Исеарчкуерихелпер::p UT \_ куеритермекспансион**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | Возвращает или задает флаг расширения критерия поиска. |



 

Этот метод позволяет раскрытие некоторых терминов запроса с подстановочными знаками, аналогично расширению регулярных выражений. Расширение префикса ищет слова с одинаковым префиксом (Fun/воронка). Если параметр не задан, по умолчанию используется \_ значение \_ префикс условия поиска \_ . Ниже приведены поддерживаемые значения перечисления [**для \_ \_ расширения условий поиска**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) .

-   Поиск \_ по \_ префиксу слова \_ ALL — развернуты все условия поиска
-   Поиск \_ слова \_ без \_ расширения — условия поиска не развернуты

## <a name="working-with-other-isearchqueryhelper-methods"></a>Работа с другими методами Исеарчкуерихелпер

Многие методы в интерфейсе [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) используются для задания аргументов запроса или определения возвращаемых свойств.



| Методы                                                                                                                                                                                                                                                 | Описание                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Исеарчкуерихелпер:: Get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | Возвращает строку подключения OLE DB. Это предпочтительный метод получения правильно отформатированной и правильной строки подключения.                                  |
| [**Исеарчкуерихелпер:: Get \_ куеримаксресултс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [**Исеарчкуерихелпер::p UT \_ куеримаксресултс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | Возвращает или задает максимальное число результатов, возвращаемых запросом (то есть выберите TOP n). Значение по умолчанию равно-1, то есть предложение максимального результата не создается. |
| [**Исеарчкуерихелпер:: Get \_ куерисортинг**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [**Исеарчкуерихелпер::p UT \_ куерисортинг**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | Возвращает или задает порядок сортировки для результирующего набора запроса (ORDER BY). Если предложение ORDER BY не существует, результаты возвращаются в недетерминированном порядке.                   |
| [**Исеарчкуерихелпер:: Get \_ куерисинтакс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [**Исеарчкуерихелпер::p UT \_ куерисинтакс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | Возвращает или задает синтаксис запроса: расширенный синтаксис запроса или синтаксис естественного запроса.                                                                                  |
| [**Исеарчкуерихелпер:: Get \_ куеривхеререстриктионс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [**Исеарчкуерихелпер::p UT \_ куеривхеререстриктионс**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | Возвращает или задает ограничения, добавляемые с помощью предложения WHERE.                                                                                                             |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отправка программных запросов к индексу](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[использование SQL и подходов акс для запроса индекса](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Запрос индекса с помощью протокола Search-MS](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[запрос к индексу с помощью Windows поискового синтаксиса SQL](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Использование расширенного синтаксиса запросов программными средствами](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




