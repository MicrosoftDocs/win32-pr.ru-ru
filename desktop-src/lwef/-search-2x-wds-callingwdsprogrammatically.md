---
title: Программный вызов WDS
description: Microsoft Windows Desktop Search (WDS) 2. x можно запрашивать программно с помощью методов ExecuteQuery и ексекутесклкуери в интерфейсе исеарчдесктоп.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8879001bcf284affd03ff472ac9327445b799acd44465b5bae9a8cb2d819b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976904"
---
# <a name="calling-wds-programmatically"></a>Программный вызов WDS

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [Windows поиск](../search/-search-3x-wds-overview.md) .

Microsoft Windows Desktop Search (WDS) 2. x можно запрашивать программно с помощью методов **ExecuteQuery** и **ексекутесклкуери** в интерфейсе [**исеарчдесктоп**](/previous-versions//aa965729(v=vs.85)) . Метод **ExecuteQuery** возвращает набор записей из индекса на основе текста запроса, столбцов и ограничений, переданных в качестве параметров. метод **ексекутесклкуери** также возвращает набор записей результатов, но требует передачи точной команды язык SQL (SQL). В большинстве случаев следует использовать **ExecuteQuery** .

## <a name="regular-queries"></a>Обычные запросы

Обычные запросы — это данные, введенные пользователем в поле ввода WDS, включая [синтаксис расширенных запросов](-search-2x-wds-aqsreference.md). Запрос передается в **ExecuteQuery** вместе со столбцами [схемы](-search-2x-wds-schematable.md) WDS 2. x для возврата, столбца и порядка сортировки результатов и любых предложений для ограничения результатов.

Метод имеет вид:

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Направление | Переменная           | Описание                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| В        | лпквстркуери       | Текст запроса. этот запрос аналогичен запросу, введенному в текстовое поле поиска в Windows пользовательском интерфейсе поиска на рабочем столе. <br/> Пример: `"from:Zara dinner plans"`<br/> |
| В        | лпквстрколумн      | Включаемые столбцы, разделенные запятыми. <br/> Пример: `"DocTitle, Url"`<br/>                                                                                            |
| В        | лпквстрсорт        | Столбец переопределения для сортировки по, за которым следует ASC для Ascending или DESC для нисходящей. <br/> Пример: `"LastAuthor DESC"`<br/>                                                  |
| В        | лпквстррестриктион | ограничения, добавляемые с помощью предложений where в Windows "поиск на рабочем столе" выберите. <br/> Пример: `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| Исходящий       | ппирс              | Результирующий набор записей<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>Запросы SQL

Метод **ISearchDesktop.Exeкутесклкуери** используется для отправки прямых запросов к базе данных WDS. синтаксис для запросов подобен тому, который использовался для SharePoint Server, а также возможность использовать предложения GROUP BY в стиле монарх SQL. Запрос выполняется для индекса точно так же, как он передается без дополнительной обработки расширенного синтаксиса запросов, как это делает API ExecuteQuery.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

Метод имеет вид:

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Направление | Переменная   | Описание                                    |
|-----------|------------|------------------------------------------------|
| В        | лпквстрскл | SQL запрос для выполнения по индексу WDS |
| Исходящий       | ппирс      | Результирующий набор записей                       |



 

Ресурсы:

-   Файлы поддержки для интерфейса Исеарчдесктоп: https://addins.msn.com/support/WDSSDK.zip
-   Пример Исеарчдесктоп C#: https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>Пример кода C++

> [!Note]
>
> ЭТОТ КОД И ИНФОРМАЦИЯ ПРЕДОСТАВЛЯЮТСЯ "КАК ЕСТЬ" БЕЗ КАКИХ-ЛИБО ЯВНЫХ ИЛИ ПОДРАЗУМЕВАЕМЫХ ГАРАНТИЙ, ВКЛЮЧАЯ, НО НЕ ОГРАНИЧИВАЯСЬ ПОДРАЗУМЕВАЕМЫМИ ГАРАНТИЯМИ ПРИГОДНОСТИ И (ИЛИ) ПРИГОДНОСТИ ДЛЯ КОНКРЕТНОЙ ЦЕЛИ.
>
> (C) корпорация Майкрософт (Microsoft Corporation). All rights reserved.

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Синтаксис расширенных запросов](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Наблюдаемые типы](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Вызов WDS из веб-страниц](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

