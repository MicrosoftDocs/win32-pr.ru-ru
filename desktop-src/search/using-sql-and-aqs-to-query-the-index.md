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
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a><span data-ttu-id="e33f5-104">Использование методов SQL и АКС для запроса индекса</span><span class="sxs-lookup"><span data-stu-id="e33f5-104">Using SQL and AQS Approaches to Query the Index</span></span>

<span data-ttu-id="e33f5-105">Существует несколько способов использования службы поиска Windows для запроса индекса.</span><span class="sxs-lookup"><span data-stu-id="e33f5-105">There are several ways to use Windows Search to query the index.</span></span> <span data-ttu-id="e33f5-106">В этом разделе описаны методы расширенного синтаксиса запросов (АКС) и подходов на основе язык SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="e33f5-106">This topic outlines Advanced Query Syntax (AQS) and Structured Query Language (SQL) based approaches.</span></span>

<span data-ttu-id="e33f5-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e33f5-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="e33f5-108">Запросы на основе SQL</span><span class="sxs-lookup"><span data-stu-id="e33f5-108">SQL Based Queries</span></span>](#sql-based-queries)
  - [<span data-ttu-id="e33f5-109">Использование OLE DB</span><span class="sxs-lookup"><span data-stu-id="e33f5-109">Using OLE DB</span></span>](#using-ole-db)
  - [<span data-ttu-id="e33f5-110">Использование ADO и ADO.NET</span><span class="sxs-lookup"><span data-stu-id="e33f5-110">Using ADO and ADO.NET</span></span>](#using-ado-and-adonet)
  - [<span data-ttu-id="e33f5-111">Использование SQL в локальных и удаленных запросах</span><span class="sxs-lookup"><span data-stu-id="e33f5-111">Using SQL in Local and Remote Queries</span></span>](#using-sql-in-local-and-remote-queries)
- [<span data-ttu-id="e33f5-112">Запросы на основе АКС</span><span class="sxs-lookup"><span data-stu-id="e33f5-112">AQS Based Queries</span></span>](#aqs-based-queries)
  - [<span data-ttu-id="e33f5-113">Использование Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="e33f5-113">Using ISearchQueryHelper</span></span>](#using-isearchqueryhelper)
  - [<span data-ttu-id="e33f5-114">Использование протокола Search-MS</span><span class="sxs-lookup"><span data-stu-id="e33f5-114">Using the search-ms Protocol</span></span>](#using-the-search-ms-protocol)
- [<span data-ttu-id="e33f5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e33f5-115">Related topics</span></span>](#related-topics)

## <a name="sql-based-queries"></a><span data-ttu-id="e33f5-116">Запросы на основе SQL</span><span class="sxs-lookup"><span data-stu-id="e33f5-116">SQL Based Queries</span></span>

<span data-ttu-id="e33f5-117">SQL — это язык текста, определяющий запросы.</span><span class="sxs-lookup"><span data-stu-id="e33f5-117">SQL is a text language that defines queries.</span></span> <span data-ttu-id="e33f5-118">SQL является общим для различных технологий баз данных.</span><span class="sxs-lookup"><span data-stu-id="e33f5-118">SQL is common across many different database technologies.</span></span> <span data-ttu-id="e33f5-119">Поиск Windows использует SQL, реализует его подмножество и расширяет его путем добавления элементов на язык.</span><span class="sxs-lookup"><span data-stu-id="e33f5-119">Windows Search uses SQL, implements a subset of it, and extends it by adding elements to the language.</span></span> <span data-ttu-id="e33f5-120">SQL Search, используемый службой поиска Windows, расширяет части стандартного синтаксиса запросов к базе данных SQL-92 и SQL-99, что позволяет повысить его полезность при поиске на основе текста.</span><span class="sxs-lookup"><span data-stu-id="e33f5-120">The Windows Search SQL used by Windows Search extends portions of the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span> <span data-ttu-id="e33f5-121">Все функции SQL службы поиска Windows совместимы с Windows Search в Windows XP и Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e33f5-121">All features of Windows Search SQL are compatible with Windows Search on Windows XP and Windows Server 2003, and later.</span></span>

<span data-ttu-id="e33f5-122">Дополнительные сведения об использовании синтаксиса SQL для службы поиска Windows см. [в разделе Запрос индекса с помощью синтаксиса SQL для поиска Windows](-search-sql-windowssearch-entry.md) и [обзор синтаксиса SQL Search](-search-sql-ovwofsearchquery.md).</span><span class="sxs-lookup"><span data-stu-id="e33f5-122">For more information about using Windows Search SQL syntax, see [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md) and [Overview of Windows Search SQL Syntax](-search-sql-ovwofsearchquery.md).</span></span>

<span data-ttu-id="e33f5-123">Следующие подходы к запросам индекса основаны на SQL.</span><span class="sxs-lookup"><span data-stu-id="e33f5-123">The following approaches for querying the index are SQL based.</span></span>

### <a name="using-ole-db"></a><span data-ttu-id="e33f5-124">Использование OLE DB</span><span class="sxs-lookup"><span data-stu-id="e33f5-124">Using OLE DB</span></span>

<span data-ttu-id="e33f5-125">База данных для связывания и внедрения объектов (OLE DB) — это API COM, который позволяет единообразно обращаться к различным типам хранилищ данных, включая нереляционные базы данных, такие как электронные таблицы.</span><span class="sxs-lookup"><span data-stu-id="e33f5-125">The Object Linking and Embedding Database (OLE DB) is a Component Object Model (COM) API that enables you to access different types of data stores uniformly, including non-relational databases like spreadsheets.</span></span> <span data-ttu-id="e33f5-126">OLE DB разделяет хранилище данных от приложения, обращающегося к нему через набор абстракций, включающих источник данных оболочки, сеанс, команду и наборы строк.</span><span class="sxs-lookup"><span data-stu-id="e33f5-126">OLE DB separates the data store from the application accessing it through a set of abstractions that include the Shell data source, session, command, and rowsets.</span></span> <span data-ttu-id="e33f5-127">Поставщик OLE DB — это программный компонент, реализующий интерфейс OLE DB для предоставления данных приложениям из определенного хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="e33f5-127">An OLE DB provider is a software component that implements the OLE DB interface to provide data to applications from a particular data store.</span></span>

<span data-ttu-id="e33f5-128">Доступ к поставщику OLE DB поиска Windows можно получить программным путем с помощью объектов OleDbConnection и Оледбсессион в C \# и с помощью встроенной поддержки OLE DB в библиотеке ATL (через атлклидб. h).</span><span class="sxs-lookup"><span data-stu-id="e33f5-128">You can access the Windows Search OLE DB provider programmatically by using the OleDbConnection and OleDbSession objects in C\# and by using the OLE DB support built into Active Template Library (ATL) in C++ (via atlclidb.h).</span></span> <span data-ttu-id="e33f5-129">Единственным свойством, которое должно быть задано, является строка поставщика.</span><span class="sxs-lookup"><span data-stu-id="e33f5-129">The only property that has to be set is the provider string.</span></span>

<span data-ttu-id="e33f5-130">Можно использовать следующую строку:</span><span class="sxs-lookup"><span data-stu-id="e33f5-130">You can use the following string:</span></span>

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

<span data-ttu-id="e33f5-131">Кроме того, строку подключения можно получить, вызвав [**исеарчкуерихелпер:: Get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="e33f5-131">Alternatively, you can get the connection string by calling [**ISearchQueryHelper::get\_ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span> <span data-ttu-id="e33f5-132">Пример см. в разделе Использование [исеарчкуерихелпер](#using-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="e33f5-132">See Using [ISearchQueryHelper](#using-isearchqueryhelper) for an example.</span></span>

> [!Note]  
> <span data-ttu-id="e33f5-133">Поставщик OLE DB поиска Windows доступен только для чтения и поддерживает инструкции SELECT и GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="e33f5-133">The Windows Search OLE DB provider is read-only, and support SELECT and GROUP ON statements.</span></span> <span data-ttu-id="e33f5-134">Инструкции INSERT и DELETE не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e33f5-134">INSERT and DELETE statements are not supported.</span></span>

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

<span data-ttu-id="e33f5-135">Дополнительные сведения о OLE DB см. в разделе [Общие сведения о программировании OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="e33f5-135">For more information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span></span> <span data-ttu-id="e33f5-136">Сведения о поставщике данных платформа .NET Framework для OLE DB см. в документации по [пространству имен System. Data. OLEDB](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .</span><span class="sxs-lookup"><span data-stu-id="e33f5-136">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) documentation.</span></span>

### <a name="using-ado-and-adonet"></a><span data-ttu-id="e33f5-137">Использование ADO и ADO.NET</span><span class="sxs-lookup"><span data-stu-id="e33f5-137">Using ADO and ADO.NET</span></span>

<span data-ttu-id="e33f5-138">Microsoft объекты данных ActiveX (ADO) и ADO.NET позволяют создавать клиентские приложения для доступа к данным на сервере базы данных и управления ими с помощью поставщика.</span><span class="sxs-lookup"><span data-stu-id="e33f5-138">Microsoft ActiveX Data Objects (ADO) and ADO.NET enable you to write client applications to access and manipulate data in a database server through a provider.</span></span> <span data-ttu-id="e33f5-139">Поиск Windows — это технология, доступная только для чтения. Вы можете получать данные с помощью поиска на рабочем столе, но нельзя изменять данные с помощью службы поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="e33f5-139">Windows Search is a read-only technology: you can retrieve data using Desktop Search but you can't change data using Windows Search.</span></span> <span data-ttu-id="e33f5-140">Однако можно передать результаты поиска в технологию, которая может изменять данные.</span><span class="sxs-lookup"><span data-stu-id="e33f5-140">You can, however, pass the results of a search over to a technology that can change data.</span></span>

<span data-ttu-id="e33f5-141">В следующих примерах кода показано, как открыть соединение с источником данных, создать и открыть набор записей с помощью инструкции SELECT [SQL в Windows Search](-search-sql-ovwofsearchquery.md) и получить URL-адреса из пяти самых крупных файлов из индекса.</span><span class="sxs-lookup"><span data-stu-id="e33f5-141">The following code examples demonstrate how to open a connection to the data source, create and open a RecordSet with a [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT statement, and get the URLs of the five largest files from the index.</span></span>

> [!Note]  
> <span data-ttu-id="e33f5-142">Сведения о том, как получить строку подключения, см. в разделе [запросы к индексу с помощью исеарчкуерихелпер](-search-3x-wds-qryidx-searchqueryhelper.md)и [исеарчкуерихелпер:: Get \_ строка подключения](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="e33f5-142">For information on how to obtain the connection string, see [Querying the Index with ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md), and [ISearchQueryHelper::get\_Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span>

#### <a name="ado-and-vbscript"></a><span data-ttu-id="e33f5-143">ADO и VBScript</span><span class="sxs-lookup"><span data-stu-id="e33f5-143">ADO and VBScript</span></span>

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

#### <a name="ado-and-c"></a><span data-ttu-id="e33f5-144">ADO и C++</span><span class="sxs-lookup"><span data-stu-id="e33f5-144">ADO and C++</span></span>

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

#### <a name="ado-and-visualbasic"></a><span data-ttu-id="e33f5-145">ADO и VisualBasic</span><span class="sxs-lookup"><span data-stu-id="e33f5-145">ADO and VisualBasic</span></span>

<span data-ttu-id="e33f5-146">Сначала добавьте ссылку на объект ADODB в проекте.</span><span class="sxs-lookup"><span data-stu-id="e33f5-146">First add a reference to ADODB in your project</span></span>

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

#### <a name="adonet-and-c"></a><span data-ttu-id="e33f5-147">ADO.NET и C\#</span><span class="sxs-lookup"><span data-stu-id="e33f5-147">ADO.NET and C\#</span></span>

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

### <a name="using-sql-in-local-and-remote-queries"></a><span data-ttu-id="e33f5-148">Использование SQL в локальных и удаленных запросах</span><span class="sxs-lookup"><span data-stu-id="e33f5-148">Using SQL in Local and Remote Queries</span></span>

<span data-ttu-id="e33f5-149">Запросы можно выполнять как локально, так и удаленно.</span><span class="sxs-lookup"><span data-stu-id="e33f5-149">You can execute your queries either locally or remotely.</span></span> <span data-ttu-id="e33f5-150">В следующем примере показан локальный запрос с [предложением from](-search-sql-from.md) .</span><span class="sxs-lookup"><span data-stu-id="e33f5-150">A local query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="e33f5-151">Локальный запрос запрашивает только локальный каталог Системиндекс.</span><span class="sxs-lookup"><span data-stu-id="e33f5-151">A local query queries the local SystemIndex catalog only.</span></span>

```sql
FROM SystemIndex
```

<span data-ttu-id="e33f5-152">В следующем примере показан удаленный запрос с [предложением from](-search-sql-from.md) .</span><span class="sxs-lookup"><span data-stu-id="e33f5-152">A remote query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="e33f5-153">Добавление ComputerName преобразует предыдущий пример в удаленный запрос.</span><span class="sxs-lookup"><span data-stu-id="e33f5-153">Adding ComputerName transforms the previous example into a remote query.</span></span>

```sql
FROM [<ComputerName>.]SystemIndex
```

<span data-ttu-id="e33f5-154">По умолчанию в Windows XP и Windows Server 2003 не установлен Windows Search.</span><span class="sxs-lookup"><span data-stu-id="e33f5-154">By default, Windows XP and Windows Server 2003 do not have Windows Search installed.</span></span> <span data-ttu-id="e33f5-155">Только Windows Search 4 (WS4) предоставляет поддержку удаленного запроса.</span><span class="sxs-lookup"><span data-stu-id="e33f5-155">Only Windows Search 4 (WS4) provides remote query support.</span></span> <span data-ttu-id="e33f5-156">Предыдущие версии Windows Desktop Search (WDS), например 3,01 и более ранних версий, не поддерживают удаленный запрос.</span><span class="sxs-lookup"><span data-stu-id="e33f5-156">Previous versions of Windows Desktop Search (WDS), such as 3.01 and earlier, do not support remote querying.</span></span> <span data-ttu-id="e33f5-157">С помощью проводника Windows можно запрашивать локальный индекс удаленного компьютера для элементов файловой системы (элементы, обрабатываемые протоколом file:).</span><span class="sxs-lookup"><span data-stu-id="e33f5-157">With Windows Explorer you can query the local index of a remote computer for file system items (items handled by the "file:" protocol).</span></span>

<span data-ttu-id="e33f5-158">Чтобы получить элемент по удаленному запросу, элемент должен удовлетворять следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="e33f5-158">To retrieve an item by remote query, the item must meet the following requirements:</span></span>

- <span data-ttu-id="e33f5-159">Быть доступным через UNC-путь.</span><span class="sxs-lookup"><span data-stu-id="e33f5-159">Be accessible via Universal Naming Convention (UNC) path.</span></span>
- <span data-ttu-id="e33f5-160">Существует на удаленном компьютере, к которому имеет доступ клиент.</span><span class="sxs-lookup"><span data-stu-id="e33f5-160">Exist on the remote computer to which the client has access.</span></span>
- <span data-ttu-id="e33f5-161">Имеет свой набор безопасности, позволяющий клиенту иметь доступ на чтение.</span><span class="sxs-lookup"><span data-stu-id="e33f5-161">Have its security set to allow the client to have Read access.</span></span>

<span data-ttu-id="e33f5-162">В проводнике Windows есть функции для совместного использования элементов, включая общедоступный общий ресурс ( \\ \\ \\ общедоступный компьютер \\ ...) в **центре управления сетями и общим доступом**, а также общий ресурс пользователей ( \\ \\ \\ пользователей компьютеров.. \\ .) для элементов, общих через мастер общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e33f5-162">Windows Explorer has features for sharing items including a "Public" share (\\\\Machine\\Public\\...) in the **Network and Sharing Center**, and a "Users" share (\\\\Machine\\Users\\...) for items shared through the Sharing Wizard.</span></span> <span data-ttu-id="e33f5-163">После предоставления общего доступа к папкам можно запросить локальный индекс, указав имя компьютера удаленного компьютера в предложении FROM, и UNC-путь на удаленном компьютере в предложении SCOPE, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="e33f5-163">After you share the folder(s), you can query the local index by specifying the remote computer's machine name in the FROM clause, and a UNC path on the remote machine in the SCOPE clause, as shown in the following example:</span></span>

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a><span data-ttu-id="e33f5-164">Запросы на основе АКС</span><span class="sxs-lookup"><span data-stu-id="e33f5-164">AQS Based Queries</span></span>

<span data-ttu-id="e33f5-165">АКС — это синтаксис запроса по умолчанию, используемый службой поиска Windows для запроса индекса и уточнения и сужения параметров поиска.</span><span class="sxs-lookup"><span data-stu-id="e33f5-165">AQS is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="e33f5-166">Хотя АКС в основном работает, разработчики могут создавать запросы программным способом.</span><span class="sxs-lookup"><span data-stu-id="e33f5-166">While AQS is primarily user facing, it can be used by developers to build queries programmatically.</span></span> <span data-ttu-id="e33f5-167">В Windows 7 каноническая АКС была введена и должна использоваться в Windows 7 и более поздних версиях для программного создания запросов АКС.</span><span class="sxs-lookup"><span data-stu-id="e33f5-167">In Windows 7 canonical AQS was introduced, and must be used in Windows 7 and later, to programmatically generate AQS queries.</span></span> <span data-ttu-id="e33f5-168">Подробные сведения о АКС см. в разделе [Использование расширенного синтаксиса запросов программным способом](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="e33f5-168">For detailed information on AQS, see [Using Advanced Query Syntax Programmatically](-search-3x-advancedquerysyntax.md).</span></span>

<span data-ttu-id="e33f5-169">Следующие подходы к запросам индекса основаны на АКС.</span><span class="sxs-lookup"><span data-stu-id="e33f5-169">The following approaches for querying the index are AQS based.</span></span>

### <a name="using-isearchqueryhelper"></a><span data-ttu-id="e33f5-170">Использование Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="e33f5-170">Using ISearchQueryHelper</span></span>

<span data-ttu-id="e33f5-171">Можно разработать компонент или вспомогательный класс для запроса индекса с помощью интерфейса [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , который позволяет воспользоваться преимуществами некоторых функций системы и упростить использование службы поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="e33f5-171">You can develop a component or helper class to query the index by using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, which enables you to take advantage of some features of the system and simplify your use of Windows Search.</span></span> <span data-ttu-id="e33f5-172">Этот интерфейс помогает:</span><span class="sxs-lookup"><span data-stu-id="e33f5-172">This interface helps you:</span></span>

- <span data-ttu-id="e33f5-173">Получите строку подключения OLE DB для подключения к базе данных Windows Search.</span><span class="sxs-lookup"><span data-stu-id="e33f5-173">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
- <span data-ttu-id="e33f5-174">Преобразование запросов пользователей из АКС в SQL Search в Windows.</span><span class="sxs-lookup"><span data-stu-id="e33f5-174">Convert user queries from AQS to Windows Search SQL.</span></span>

<span data-ttu-id="e33f5-175">Этот интерфейс реализуется как вспомогательный класс для [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) и получен путем вызова [**Исеарчкаталогманажер:: жеткуерихелпер**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), как показано в следующем примере C++.</span><span class="sxs-lookup"><span data-stu-id="e33f5-175">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), as shown in the following C++ example.</span></span>

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

<span data-ttu-id="e33f5-176">Сведения о реализации интерфейса [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) см. в разделе [Использование интерфейса исеарчкуерихелпер](-search-3x-wds-qryidx-searchqueryhelper.md) и справочной статьи по [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="e33f5-176">To implement the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, see [Using the ISearchQueryHelper Interface](-search-3x-wds-qryidx-searchqueryhelper.md) and the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) reference topic.</span></span>

> [!Note]  
> <span data-ttu-id="e33f5-177">Традиционная совместимость Microsoft Windows Desktop Search (WDS) 2x: на компьютерах под управлением Windows XP и Windows Server 2003 и более поздних версий [**исеарчдесктоп**](/previous-versions//aa965729(v=vs.85)) является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="e33f5-177">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and Windows Server 2003 and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="e33f5-178">Вместо этого разработчики должны использовать [**исеарчкуерихелпер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) для получения строки подключения, анализа запроса пользователя в SQL, а затем выполнить запрос через OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e33f5-178">Instead, developers should use [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string, parse the user's query into SQL, and then query through OLE DB.</span></span>

### <a name="using-the-search-ms-protocol"></a><span data-ttu-id="e33f5-179">Использование протокола Search-MS</span><span class="sxs-lookup"><span data-stu-id="e33f5-179">Using the search-ms Protocol</span></span>

<span data-ttu-id="e33f5-180">Протокол **поиска — MS** [](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) — это соглашение для запуска приложения, например проводника Windows, для запроса индекса поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="e33f5-180">The **search-ms** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for starting an application, like Windows Explorer, to query the Windows Search index.</span></span> <span data-ttu-id="e33f5-181">Он позволяет создавать запросы с аргументами "параметр-значение", включая аргументы свойств, ранее сохраненные поисковые запросы, синтаксис расширенных запросов (АКС), синтаксис естественного запроса (НКС) и идентификаторы кода языка (LCID) для индексатора и самого запроса.</span><span class="sxs-lookup"><span data-stu-id="e33f5-181">It enables queries to be built with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="e33f5-182">Подробные сведения о синтаксисе протокола Search-MS см. [в разделе Запрос индекса с помощью протокола Search-MS](-search-3x-wds-qryidx-searchms.md).</span><span class="sxs-lookup"><span data-stu-id="e33f5-182">For detailed information on the search-ms protocol syntax, see [Querying the Index with the search-ms Protocol](-search-3x-wds-qryidx-searchms.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e33f5-183">См. также</span><span class="sxs-lookup"><span data-stu-id="e33f5-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e33f5-184">Отправка программных запросов к индексу</span><span class="sxs-lookup"><span data-stu-id="e33f5-184">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="e33f5-185">Запрос индекса с помощью Исеарчкуерихелпер</span><span class="sxs-lookup"><span data-stu-id="e33f5-185">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="e33f5-186">Запрос индекса с помощью протокола Search-MS</span><span class="sxs-lookup"><span data-stu-id="e33f5-186">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="e33f5-187">Запрос к индексу с помощью синтаксиса SQL для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="e33f5-187">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="e33f5-188">Использование расширенного синтаксиса запросов программными средствами</span><span class="sxs-lookup"><span data-stu-id="e33f5-188">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>
