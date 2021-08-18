---
description: описание появления определения приоритетов индексирования и событий набора строк для Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: определение приоритетов индексирования и событий набора строк в Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92491300127c60ebdf2a265583fca77e77a09907b7f42b471f6d3d047a7f6aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680505"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>определение приоритетов индексирования и событий набора строк в Windows 7

в этом разделе описаны общие сведения о приоритетах индексирования и событиях наборов строк для Windows 7.

Этот раздел организован следующим образом:

-   [Определение приоритетов индексирования и события набора строк](#indexing-prioritization-and-rowset-events)
    -   [Примеры Ировсетприоризатион](#irowsetpriorization-examples)
    -   [События Ировсетприоритизатион](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Дополнительные ресурсы](#additional-resources)
-   [Связанные темы](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Определение приоритетов индексирования и события набора строк

в Windows 7 и более поздних версиях имеется стек приоритетов, в котором контекст любого конкретного запроса, клиент может запросить, чтобы области, используемые в этом запросе, были назначены по приоритету выше, чем обычные элементы.

Этот стек приоритетов имеет следующие характеристики.

-   Элементы в стеке могут иметь передний план, высокий или низкий приоритет:
    -   **Передний план**: логика отхода пропускается, и индексирование выполняется так же быстро, как это разрешено для компьютера.
    -   **Высокий**: приоритет был запрошен с помощью отхода.
    -   **Низкий**: запрошено определение приоритетов, а не затраты на другие области в стеке, но выше индексирование без приоритизации.
-   Любой запрос приоритета High или переднего плана перемещает запрос к верхней части стека автоматически.
-   Приоритет переднего плана может иметь только элемент поверх стека.
-   Запрос с приоритетом переднего плана, который передается по приоритету, получает событие с уведомлением о том, что он потерял приоритет переднего плана и стал высоким приоритетом с отходом.

В стеке приоритетов задается общий приоритет элементов, обрабатываемых в индексаторе следующим образом:

-   Уведомления с высоким приоритетом не обрабатываются и обычно отправляются только для небольшого числа элементов. например, Windows Explorer использует этот приоритет для малых операций с подсистемой копирования.
-   Стек приоритетов находится на вершине стека, имеет откладывание и является последним запрошенным запросом приоритета.
-   Второй запрос в стеке.
-   Третий запрос в стеке.
-   Четвертый запрос в стеке и т. д.
-   Элементы с нормальным приоритетом.
-   Удаленные элементы.
    > [!Note]  
    > Элементы внутри каждой группы задаются внутренне по приоритету с использованием старой семантики для каждого элемента.

     

### <a name="irowsetpriorization-examples"></a>Примеры Ировсетприоризатион

Основной API для работы с приоритетами доступен через следующий интерфейс, который можно вызвать, выполнив запрос к возвращенному набору строк:


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



Приоритеты наборов строк работают следующим образом:

1.  [**Ировсетприоритизатион**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) получен с помощью [метода IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в наборе строк индексатора. **DBPROP \_ Для ЕНАБЛЕРОВСЕТЕВЕНТС** необходимо задать значение **true** с помощью метода OLE DB [ICommandProperties:: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) перед выполнением запроса, чтобы использовать определение приоритета набора строк.
2.  [**Ировсетприоритизатион:: сетскопеприорити**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) задает приоритет для областей, принадлежащих запросу, и интервал, который вызывается событием статистики области при наличии необработанных документов для индексирования в областях запроса. Это событие возникает, если для уровня приоритета задано значение по умолчанию.
3.  [**Ировсетприоритизатион:: жетскопестатистикс**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) можно использовать для получения количества индексированных элементов в области, количества необработанных документов, которые необходимо добавить в область, и количества документов, которые необходимо повторно индексировать в этой области.

### <a name="irowsetprioritization-events"></a>События Ировсетприоритизатион

Существует три события набора строк в [**ировсетевентс:: онровсетевент**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) в перечислении [**\_ типа ровсетевент**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



Ниже приведены события набора строк.

-   Событие **ровсетевент \_ типа данных с \_ истекшим сроком действия** указывает на то, что срок действия набора строк истек, и что необходимо запросить новый набор строк.
-   Событие **\_ \_ Фореграундлост типа набора строк** указывает, что элемент, имеющий приоритет переднего плана в стеке приоритизации, был понижен, так как кто-то другой заранее определил приоритеты этого запроса.
-   Событие **\_ \_ скопестатистикс типа ровсетевент** предоставляет те же сведения, что и при вызове метода [**ировсетприоритизатион:: жетскопестатистикс**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , но с помощью Push-механику следующим образом:
    -   Событие возникает, если API приоритизации использовался для запроса уровня приоритетности, отличного от значения по умолчанию, и частоты событий статистики, отличной от нулевой.
    -   Событие возникает только при фактическом изменении статистики и интервале, указанном в [**ировсетприоритизатион**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) (интервал не гарантирует частоту события).
    -   Это событие гарантированно вызовет состояние "возврат к нулю" (для добавления нулевых элементов, оставшиеся нулевые изменения) при условии, что было вызвано ненулевое событие.
    -   Индексатор может обрабатывать элементы без отправки этого события, если очередь очищается до частоты событий статистики.

## <a name="additional-resources"></a>Дополнительные ресурсы

См. следующие ресурсы, связанные с определением приоритетов и наборами строк.

-   Интерфейсы:
    -   [**ировсетевентс**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**ировсетприоритизатион**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Перечисления:
    -   [**определение приоритетов \_ флагов**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**уровень ПРИОРИТЕТа \_**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**РОВСЕТЕВЕНТ \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**\_тип ровсетевент**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[поиск Windows 7](./-search-3x-wds-overview.md)
</dt> <dt>

[новые сведения для поиска Windows 7](new-for-windows-7-search.md)
</dt> <dt>

[Windows библиотеки оболочки в Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 