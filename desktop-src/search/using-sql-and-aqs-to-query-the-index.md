---
description: Существует несколько способов использования службы поиска Windows для запроса индекса. В этом разделе описаны методы расширенного синтаксиса запросов (АКС) и подходов на основе язык SQL (SQL).
ms.assetid: 544f03b3-cdf8-4550-a6da-e4a3bfc44744
title: Использование методов SQL и АКС для запроса индекса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641bea0e6109182b5896aa1f0f981695fd91b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692159"
---
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a>Использование методов SQL и АКС для запроса индекса

Существует несколько способов использования службы поиска Windows для запроса индекса. В этом разделе описаны методы расширенного синтаксиса запросов (АКС) и подходов на основе язык SQL (SQL).

Этот раздел организован следующим образом:

- [Запросы на основе SQL](#sql-based-queries)
  - [Использование OLE DB](#using-ole-db)
  - [Использование ADO и ADO.NET](#using-ado-and-adonet)
  - [Использование SQL в локальных и удаленных запросах](#using-sql-in-local-and-remote-queries)
- [Запросы на основе АКС](#aqs-based-queries)
  - [Использование Исеарчкуерихелпер](#using-isearchqueryhelper)
  - [Использование протокола Search-MS](#using-the-search-ms-protocol)
- [См. также](#related-topics)

## <a name="sql-based-queries"></a>Запросы на основе SQL

SQL — это язык текста, определяющий запросы. SQL является общим для различных технологий баз данных. Поиск Windows использует SQL, реализует его подмножество и расширяет его путем добавления элементов на язык. SQL Search, используемый службой поиска Windows, расширяет части стандартного синтаксиса запросов к базе данных SQL-92 и SQL-99, что позволяет повысить его полезность при поиске на основе текста. Все функции SQL службы поиска Windows совместимы с Windows Search в Windows XP и Windows Server 2003 и более поздних версиях.

Дополнительные сведения об использовании синтаксиса SQL для службы поиска Windows см. [в разделе Запрос индекса с помощью синтаксиса SQL для поиска Windows](-search-sql-windowssearch-entry.md) и [обзор синтаксиса SQL Search](-search-sql-ovwofsearchquery.md).

Следующие подходы к запросам индекса основаны на SQL.

### <a name="using-ole-db"></a>Использование OLE DB

База данных для связывания и внедрения объектов (OLE DB) — это API COM, который позволяет единообразно обращаться к различным типам хранилищ данных, включая нереляционные базы данных, такие как электронные таблицы. OLE DB разделяет хранилище данных от приложения, обращающегося к нему через набор абстракций, включающих источник данных оболочки, сеанс, команду и наборы строк. Поставщик OLE DB — это программный компонент, реализующий интерфейс OLE DB для предоставления данных приложениям из определенного хранилища данных.

Доступ к поставщику OLE DB поиска Windows можно получить программным путем с помощью объектов OleDbConnection и Оледбсессион в C \# и с помощью встроенной поддержки OLE DB в библиотеке ATL (через атлклидб. h). Единственным свойством, которое должно быть задано, является строка поставщика.

Можно использовать следующую строку:

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

Кроме того, строку подключения можно получить, вызвав [**исеарчкуерихелпер:: Get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring). Пример см. в разделе Использование [исеарчкуерихелпер](#using-isearchqueryhelper) .

> [!Note]  
> Поставщик OLE DB поиска Windows доступен только для чтения и поддерживает инструкции SELECT и GROUP ON. Инструкции INSERT и DELETE не поддерживаются.

```cpp
#include <atldbcli.h>
CDataSource cDataSource;
hr = cDataSource.OpenFromInitializationString(L"provider=Search.CollatorDSO.1;EXTENDED PROPERTIES=\"Application=Windows\"");

if (SUCCEEDED(hr))
{
    CSession cSession;
    hr = cSession.Open(cDataSource);

    if (SUCCEEDED(hr))
    {
        CCommand<CDynamicAccessor, CRowset> cCommand;
        hr = cCommand.Open(cSession, pszSQL);

        if (SUCCEEDED(hr))
        {
            for (hr = cCommand.MoveFirst(); S_OK == hr; hr = cCommand.MoveNext())
            {
                for (DBORDINAL i = 1; i <= cCommand.GetColumnCount(); i++)
                {
                    PCWSTR pszName = cCommand.GetColumnName(i);
                    // do something with the column here
                }
            }
            cCommand.Close();
        }
    }
}
```

Дополнительные сведения о OLE DB см. в разделе [Общие сведения о программировании OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx). Сведения о поставщике данных платформа .NET Framework для OLE DB см. в документации по [пространству имен System. Data. OLEDB](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .

### <a name="using-ado-and-adonet"></a>Использование ADO и ADO.NET

Microsoft объекты данных ActiveX (ADO) и ADO.NET позволяют создавать клиентские приложения для доступа к данным на сервере базы данных и управления ими с помощью поставщика. Поиск Windows — это технология, доступная только для чтения. Вы можете получать данные с помощью поиска на рабочем столе, но нельзя изменять данные с помощью службы поиска Windows. Однако можно передать результаты поиска в технологию, которая может изменять данные.

В следующих примерах кода показано, как открыть соединение с источником данных, создать и открыть набор записей с помощью инструкции SELECT [SQL в Windows Search](-search-sql-ovwofsearchquery.md) и получить URL-адреса из пяти самых крупных файлов из индекса.

> [!Note]  
> Сведения о том, как получить строку подключения, см. в разделе [запросы к индексу с помощью исеарчкуерихелпер](-search-3x-wds-qryidx-searchqueryhelper.md)и [исеарчкуерихелпер:: Get \_ строка подключения](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).

#### <a name="ado-and-vbscript"></a>ADO и VBScript

```VB
'To run this snippet, save it to a file and run it using cscript.exe from a command line.
'Running the .vbs file with Windows Script Host may cause dialog boxes to open for each item returned from the index.

On Error Resume Next

Set objConnection = CreateObject("ADODB.Connection")
Set objRecordSet = CreateObject("ADODB.Recordset")

objConnection.Open "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"

objRecordSet.Open "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC", objConnection

objRecordSet.MoveFirst
Do Until objRecordset.EOF
    Wscript.Echo objRecordset.Fields.Item("System.ItemPathDisplay")
    objRecordset.MoveNext
Loop
```

#### <a name="ado-and-c"></a>ADO и C++

```cpp
#import "msado15.dll" rename_namespace("ADO") rename("EOF", "EndOfFile") implementation_only

ADO::_ConnectionPtr connection = NULL;
HRESULT hr = connection.CreateInstance(__uuidof(ADO::Connection));
if (SUCCEEDED(hr))
{
    ADO::_RecordsetPtr recordset = NULL;
    hr = recordset.CreateInstance(__uuidof(ADO::Recordset));
    if (SUCCEEDED(hr))
    {
        connection->CursorLocation = ADO::adUseClient;
        hr = connection->Open(L"Provider=Search.CollatorDSO;Extended Properties='Application=Windows';",
            L"", L"", ADO::adConnectUnspecified);
        if (SUCCEEDED(hr))
        {
            hr = recordset->Open("SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC",
            connection.GetInterfacePtr(), ADO::adOpenForwardOnly, ADO::adLockReadOnly, ADO::adCmdText);
            if (SUCCEEDED(hr))
            {
                while (!recordset->EndOfFile)
                {
                    _variant_t var;
                    var = recordset->Fields->GetItem(L"System.ItemPathDisplay")->GetValue();
                    std::cout << static_cast<char *>(_bstr_t(var.bstrVal)) << std::endl;
                    recordset->MoveNext();
                };
                recordset->Close();
            }
            connection->Close();
        }
    }
}

```

#### <a name="ado-and-visualbasic"></a>ADO и VisualBasic

Сначала добавьте ссылку на объект ADODB в проекте.

```VB
Dim con As ADODB.Connection
Dim rst As ADODB.Recordset

con = New ADODB.Connection
rst = New ADODB.Recordset

Dim sConString As String
Dim sSQLString As String

sConString = "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"
con.Open(sConString)

sSQLString = "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC"

rst = con.Execute(sSQLString)

Do Until (rst.EOF)
    Print(1, rst("System.ItemPathDisplay").Value)
    rst.MoveNext
Loop

rst.Close
rst = Nothing

con.Close
con = Nothing
```

#### <a name="adonet-and-c"></a>ADO.NET и C\#

```csharp
string query = @"SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC";

using (OleDbConnection objConnection =
    new OleDbConnection
    ("Provider=Search.CollatorDSO.1;Extended?Properties='Application=Windows';"))
{
    objConnection.Open();
    OleDbCommand cmd = new OleDbCommand(query, objConnection);
    using (OleDbDataReader rdr = cmd.ExecuteReader())
    {
        for (int i = 0; i < rdr.FieldCount; i++)
        {
            Console.Write(rdr.GetName(i));
            Console.Write('\t');
        }
        while (rdr.Read())
        {
            Console.WriteLine();
            for (int i = 0; i < rdr.FieldCount; i++)
            {
                Console.Write(rdr[i]);
                Console.Write('\t');
            }
        }
        Console.ReadKey();
    }
}
```

### <a name="using-sql-in-local-and-remote-queries"></a>Использование SQL в локальных и удаленных запросах

Запросы можно выполнять как локально, так и удаленно. В следующем примере показан локальный запрос с [предложением from](-search-sql-from.md) . Локальный запрос запрашивает только локальный каталог Системиндекс.

```sql
FROM SystemIndex
```

В следующем примере показан удаленный запрос с [предложением from](-search-sql-from.md) . Добавление ComputerName преобразует предыдущий пример в удаленный запрос.

```sql
FROM [<ComputerName>.]SystemIndex
```

По умолчанию в Windows XP и Windows Server 2003 не установлен Windows Search. Только Windows Search 4 (WS4) предоставляет поддержку удаленного запроса. Предыдущие версии Windows Desktop Search (WDS), например 3,01 и более ранних версий, не поддерживают удаленный запрос. С помощью проводника Windows можно запрашивать локальный индекс удаленного компьютера для элементов файловой системы (элементы, обрабатываемые протоколом file:).

Чтобы получить элемент по удаленному запросу, элемент должен удовлетворять следующим требованиям.

- Быть доступным через UNC-путь.
- Существует на удаленном компьютере, к которому имеет доступ клиент.
- Имеет свой набор безопасности, позволяющий клиенту иметь доступ на чтение.

В проводнике Windows есть функции для совместного использования элементов, включая общедоступный общий ресурс ( \\ \\ \\ общедоступный компьютер \\ ...) в **центре управления сетями и общим доступом**, а также общий ресурс пользователей ( \\ \\ \\ пользователей компьютеров.. \\ .) для элементов, общих через мастер общего доступа. После предоставления общего доступа к папкам можно запросить локальный индекс, указав имя компьютера удаленного компьютера в предложении FROM, и UNC-путь на удаленном компьютере в предложении SCOPE, как показано в следующем примере:

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a>Запросы на основе АКС

АКС — это синтаксис запроса по умолчанию, используемый службой поиска Windows для запроса индекса и уточнения и сужения параметров поиска. Хотя АКС в основном работает, разработчики могут создавать запросы программным способом. В Windows 7 каноническая АКС была введена и должна использоваться в Windows 7 и более поздних версиях для программного создания запросов АКС. Подробные сведения о АКС см. в разделе [Использование расширенного синтаксиса запросов программным способом](-search-3x-advancedquerysyntax.md).

Следующие подходы к запросам индекса основаны на АКС.

### <a name="using-isearchqueryhelper"></a>Использование Исеарчкуерихелпер

Можно разработать компонент или вспомогательный класс для запроса индекса с помощью интерфейса [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , который позволяет воспользоваться преимуществами некоторых функций системы и упростить использование службы поиска Windows. Этот интерфейс помогает:

- Получите строку подключения OLE DB для подключения к базе данных Windows Search.
- Преобразование запросов пользователей из АКС в SQL Search в Windows.

Этот интерфейс реализуется как вспомогательный класс для [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) и получен путем вызова [**Исеарчкаталогманажер:: жеткуерихелпер**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), как показано в следующем примере C++.

```cpp
HRESULT GetQueryHelper(ISearchQueryHelper **ppQueryHelper)
{
    *ppQueryHelper = NULL;

    // Create an instance of the search manager

    ISearchManager *pSearchManager;
    HRESULT hr = CoCreateInstance(__uuidof(CSearchManager), NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));
    if (SUCCEEDED(hr))
    {
        // Get the catalog manager from the search manager
        ISearchCatalogManager *pSearchCatalogManager;
        hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
        if (SUCCEEDED(hr))
        {
            // Get the query helper from the catalog manager
            hr = pSearchCatalogManager->GetQueryHelper(ppQueryHelper);
            pSearchCatalogManager->Release();
        }
        pSearchManager->Release();
    }

    return hr;
}
```

Сведения о реализации интерфейса [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) см. в разделе [Использование интерфейса исеарчкуерихелпер](-search-3x-wds-qryidx-searchqueryhelper.md) и справочной статьи по [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .

> [!Note]  
> Традиционная совместимость Microsoft Windows Desktop Search (WDS) 2x: на компьютерах под управлением Windows XP и Windows Server 2003 и более поздних версий [**исеарчдесктоп**](/previous-versions//aa965729(v=vs.85)) является устаревшим. Вместо этого разработчики должны использовать [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) для получения строки подключения, анализа запроса пользователя в SQL, а затем выполнить запрос через OLE DB.

### <a name="using-the-search-ms-protocol"></a>Использование протокола Search-MS

Протокол **поиска — MS** [](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) — это соглашение для запуска приложения, например проводника Windows, для запроса индекса поиска Windows. Он позволяет создавать запросы с аргументами "параметр-значение", включая аргументы свойств, ранее сохраненные поисковые запросы, синтаксис расширенных запросов (АКС), синтаксис естественного запроса (НКС) и идентификаторы кода языка (LCID) для индексатора и самого запроса.

Подробные сведения о синтаксисе протокола Search-MS см. [в разделе Запрос индекса с помощью протокола Search-MS](-search-3x-wds-qryidx-searchms.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Отправка программных запросов к индексу](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Запрос индекса с помощью Исеарчкуерихелпер](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Запрос индекса с помощью протокола Search-MS](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Запрос к индексу с помощью синтаксиса SQL для поиска Windows](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Использование расширенного синтаксиса запросов программными средствами](-search-3x-advancedquerysyntax.md)
</dt> </dl>
