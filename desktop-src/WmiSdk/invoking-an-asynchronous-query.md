---
description: Асинхронный запрос, который более сложен для записи, является предпочтительным типом запроса при повлиянии на производительность системы или сети путем запроса большой группы данных.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Вызов асинхронного запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a0e297c6a1955d0006d888fc95f5e827f5cb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913364"
---
# <a name="invoking-an-asynchronous-query"></a><span data-ttu-id="0d7de-103">Вызов асинхронного запроса</span><span class="sxs-lookup"><span data-stu-id="0d7de-103">Invoking an Asynchronous Query</span></span>

<span data-ttu-id="0d7de-104">Асинхронный запрос, который более сложен для записи, является предпочтительным типом запроса при повлиянии на производительность системы или сети путем запроса большой группы данных.</span><span class="sxs-lookup"><span data-stu-id="0d7de-104">An asynchronous query, while somewhat more complex to write, is the preferred type of query when system or network performance will be affected by querying a large group of data.</span></span> <span data-ttu-id="0d7de-105">В сценарии создание объекта [**свбемсинк**](swbemsink.md) и подподпрограмм для управления событиями, которые может получить приемник, являются единственными дополнительными задачами, которые выходят за пределы базового запроса.</span><span class="sxs-lookup"><span data-stu-id="0d7de-105">In script, creating an [**SWbemSink**](swbemsink.md) object and subroutines to handle the events that the sink could receive are the only additional tasks beyond the basic query.</span></span>

> [!Note]  
> <span data-ttu-id="0d7de-106">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="0d7de-106">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="0d7de-107">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0d7de-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="0d7de-108">Следующие сокращенные запросы сценариев для всех файлов данных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0d7de-108">The following abbreviated script queries for all of the data files on the local machine.</span></span> <span data-ttu-id="0d7de-109">Этот запрос может занять слишком много времени, если он был выполнен для всех компьютеров в сети.</span><span class="sxs-lookup"><span data-stu-id="0d7de-109">This query could take an excessive amount of time if it were executed for all of the machines on a network.</span></span> <span data-ttu-id="0d7de-110">Объект [**свбемсинк**](swbemsink.md) настраивается, а единственным обрабатываемым событием является oncompleteed Event.</span><span class="sxs-lookup"><span data-stu-id="0d7de-110">An [**SWbemSink**](swbemsink.md) object is set up and the only event that is handled is the OnCompleted event.</span></span>


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



<span data-ttu-id="0d7de-111">Подробные сведения о создании асинхронных вызовов методов в скрипте см. в разделе [вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0d7de-111">For detailed information about constructing asynchronous method calls in script, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0d7de-112">В приложениях C++ асинхронный запрос порождает отдельный процесс для получения данных запроса.</span><span class="sxs-lookup"><span data-stu-id="0d7de-112">In C++ applications, an asynchronous query spawns a separate process to receive query data.</span></span> <span data-ttu-id="0d7de-113">Асинхронный запрос более сложен по сравнению с синхронным запросом, так как необходимо закодировать многопоточное приложение.</span><span class="sxs-lookup"><span data-stu-id="0d7de-113">An asynchronous query is more complex than a synchronous query, as you must code a multithreaded application.</span></span> <span data-ttu-id="0d7de-114">Однако асинхронный запрос не монопольно использует основной поток приложения.</span><span class="sxs-lookup"><span data-stu-id="0d7de-114">However, an asynchronous query does not monopolize the main thread of your application.</span></span>

<span data-ttu-id="0d7de-115">В следующей процедуре описывается выполнение асинхронного запроса в C++.</span><span class="sxs-lookup"><span data-stu-id="0d7de-115">The following procedure describes how to perform an asynchronous query in C++.</span></span>

<span data-ttu-id="0d7de-116">**Выполнение асинхронного запроса в C++**</span><span class="sxs-lookup"><span data-stu-id="0d7de-116">**To perform an asynchronous query in C++**</span></span>

1.  <span data-ttu-id="0d7de-117">Реализуйте объект **ивбемсинк** .</span><span class="sxs-lookup"><span data-stu-id="0d7de-117">Implement an **IWbemSink** object.</span></span>

    <span data-ttu-id="0d7de-118">Объект **ивбемсинк** получает сведения об асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="0d7de-118">An **IWbemSink** object receives information about an asynchronous operation.</span></span>

2.  <span data-ttu-id="0d7de-119">Опишите запрос в вызове [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span><span class="sxs-lookup"><span data-stu-id="0d7de-119">Describe your query in a call to [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span></span>

    <span data-ttu-id="0d7de-120">WMI немедленно перемещает процесс, который запрашивает CIM, в другой поток и освобождает поток, который выполнил запрос для другой задачи.</span><span class="sxs-lookup"><span data-stu-id="0d7de-120">WMI immediately moves the process that queries the CIM to another thread and frees up the thread that executed the query for another task.</span></span>

3.  <span data-ttu-id="0d7de-121">Дождитесь, пока Инструментарий WMI вызовет метод [**ивбемобжектсинк:: обозначают**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="0d7de-121">Wait for WMI to call the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

    <span data-ttu-id="0d7de-122">По завершении Инструментарий WMI вызывает [**Указание**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) , чтобы сообщить приложению о завершении запроса.</span><span class="sxs-lookup"><span data-stu-id="0d7de-122">When finished, WMI calls [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to signal your application that the query is complete.</span></span> <span data-ttu-id="0d7de-123">Инструментарий WMI также возвращает результаты запроса в приемник в виде указателя на указатель интерфейса [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="0d7de-123">WMI also returns results of the query to the sink as a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="0d7de-124">Как и в случае с синхронным запросом, используйте указатель для доступа к объектам, которые составляют результат запроса.</span><span class="sxs-lookup"><span data-stu-id="0d7de-124">As with a synchronous query, use the pointer to access the objects that make up the result of your query.</span></span>

<span data-ttu-id="0d7de-125">Следующий пример кода не компилируется без ошибок, так как класс Куерисинк не определен.</span><span class="sxs-lookup"><span data-stu-id="0d7de-125">The following code example does not compile without an error because the class QuerySink has not been defined.</span></span> <span data-ttu-id="0d7de-126">Определение класса Куерисинк см. в разделе [**ивбемобжектсинк**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="0d7de-126">For the definition of the QuerySink class, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="0d7de-127">В примере кода также требуются следующие инструкции Reference и \# include.</span><span class="sxs-lookup"><span data-stu-id="0d7de-127">The code example also requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="0d7de-128">В следующем примере кода показано, как выполнить асинхронный вызов для выдаче запроса.</span><span class="sxs-lookup"><span data-stu-id="0d7de-128">The following code example shows how to make an asynchronous call to issue a query.</span></span>


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



<span data-ttu-id="0d7de-129">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0d7de-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 



