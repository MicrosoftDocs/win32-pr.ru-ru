---
title: Создание функций обратного вызова состояния
description: В этом учебнике описывается создание функции обратного вызова состояния, используемой для отслеживания состояния Интернет-запроса.
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105710405"
---
# <a name="creating-status-callback-functions"></a><span data-ttu-id="f750a-103">Создание функций обратного вызова состояния</span><span class="sxs-lookup"><span data-stu-id="f750a-103">Creating Status Callback Functions</span></span>

<span data-ttu-id="f750a-104">В этом учебнике описывается создание функции обратного вызова состояния, используемой для отслеживания состояния Интернет-запроса.</span><span class="sxs-lookup"><span data-stu-id="f750a-104">This tutorial describes how to create a status callback function used to monitor the status of an Internet request.</span></span>

<span data-ttu-id="f750a-105">Функции обратного вызова состояния получают обратные вызовы состояния для любых Интернет-запросов, которые были переданы из любой функции WinINet, которая передала ненулевое значение контекста.</span><span class="sxs-lookup"><span data-stu-id="f750a-105">Status callback functions receive status callbacks on any Internet requests that originated from any WinINet function that was passed a nonzero context value.</span></span>


<span data-ttu-id="f750a-106">Для создания функции обратного вызова состояния необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f750a-106">The following steps are necessary for creating a status callback function:</span></span>

1.  [<span data-ttu-id="f750a-107">Определите значение контекста.</span><span class="sxs-lookup"><span data-stu-id="f750a-107">Define the context value.</span></span>](#defining-the-context-value)
2.  [<span data-ttu-id="f750a-108">Создайте функцию обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-108">Create the status callback function.</span></span>](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a><span data-ttu-id="f750a-109">Определение значения контекста</span><span class="sxs-lookup"><span data-stu-id="f750a-109">Defining the Context Value</span></span>

<span data-ttu-id="f750a-110">Значением контекста может быть любое длинное целочисленное значение без знака.</span><span class="sxs-lookup"><span data-stu-id="f750a-110">The context value can be any unsigned long integer value.</span></span> <span data-ttu-id="f750a-111">В идеале значение контекста должно определить, какой запрос был только что выполнен, и расположение связанных ресурсов, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="f750a-111">Ideally, the context value should identify what request has just been completed and the location of any associated resources, if needed.</span></span>

<span data-ttu-id="f750a-112">Одним из наиболее полезных способов использования контекстного значения является передача адреса структуры и его приведение к типу **DWORD \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="f750a-112">One of the most useful ways to use the context value is to pass the address of a structure and cast it to a **DWORD\_PTR**.</span></span> <span data-ttu-id="f750a-113">Структуру можно использовать для хранения сведений о запросе, чтобы он был передан функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-113">The structure can be used to store information about the request, so that it is passed to the status callback function.</span></span>

<span data-ttu-id="f750a-114">Следующая структура является примером возможного значения контекста.</span><span class="sxs-lookup"><span data-stu-id="f750a-114">The following structure is an example of a possible context value.</span></span> <span data-ttu-id="f750a-115">Элементы структуры выбираются с учетом функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="f750a-115">The members of the structure are chosen with the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function in mind.</span></span>


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



<span data-ttu-id="f750a-116">В этом примере функция обратного вызова состояния будет иметь доступ к маркеру окна, что позволит отобразить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f750a-116">In this example, the status callback function would have access to the window handle, which would allow it to display a user interface.</span></span> <span data-ttu-id="f750a-117">Созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) обработчик [**хинтернет**](appendix-a-hinternet-handles.md) может быть передан другой функции, которая может загрузить ресурс и массив символов, которые можно использовать для передачи сведений о запросе.</span><span class="sxs-lookup"><span data-stu-id="f750a-117">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) could be passed to another function that can download the resource and an array of characters that can be used to pass information about the request.</span></span>

<span data-ttu-id="f750a-118">Члены структуры могут быть изменены в соответствии с потребностями конкретного приложения, поэтому в данном примере это не ограничено.</span><span class="sxs-lookup"><span data-stu-id="f750a-118">The members of the structure can be changed to fit the needs of a particular application, so do not feel constrained by this example.</span></span>

### <a name="creating-the-status-callback-function"></a><span data-ttu-id="f750a-119">Создание функции обратного вызова состояния</span><span class="sxs-lookup"><span data-stu-id="f750a-119">Creating the Status Callback Function</span></span>

<span data-ttu-id="f750a-120">Функция обратного вызова состояния должна соответствовать формату [*интернетстатускаллбакк*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span><span class="sxs-lookup"><span data-stu-id="f750a-120">The status callback function must follow the format of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span> <span data-ttu-id="f750a-121">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f750a-121">To do this:</span></span>

1.  <span data-ttu-id="f750a-122">Напишите объявление функции для функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-122">Write a function declaration for your status callback function.</span></span>

    <span data-ttu-id="f750a-123">В следующем примере показан пример объявления.</span><span class="sxs-lookup"><span data-stu-id="f750a-123">The following example shows a sample declaration.</span></span>

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  <span data-ttu-id="f750a-124">Определите, что будет делать функция обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-124">Determine what your status callback function will do.</span></span> <span data-ttu-id="f750a-125">Для приложений, выполняющих асинхронные вызовы, функция обратного вызова состояния должна поддерживать \_ \_ значение завершения запроса состояния Интернета \_ , которое указывает на то, что асинхронный запрос завершен.</span><span class="sxs-lookup"><span data-stu-id="f750a-125">For applications that are making asynchronous calls, the status callback function must handle the INTERNET\_STATUS\_REQUEST\_COMPLETE value, which indicates an asynchronous request is complete.</span></span> <span data-ttu-id="f750a-126">Функцию обратного вызова состояния также можно использовать для отслеживания хода выполнения Интернет запроса.</span><span class="sxs-lookup"><span data-stu-id="f750a-126">The status callback function can also be used to track the progress of an Internet request.</span></span>

    <span data-ttu-id="f750a-127">Как правило, лучше использовать оператор switch с *двинтернетстатус* в качестве значения переключателя и значений состояния для инструкций CASE.</span><span class="sxs-lookup"><span data-stu-id="f750a-127">In general, it works best to use a switch statement with *dwInternetStatus* as the switch value and the status values for the case statements.</span></span> <span data-ttu-id="f750a-128">В зависимости от типов функций, которые вызывает приложение, можно игнорировать некоторые значения состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-128">Depending on the types of functions your application is calling, you can ignore some of the status values.</span></span> <span data-ttu-id="f750a-129">Определение различных значений состояния см. в списке под параметром *двинтернетстатус* в [*интернетстатускаллбакк*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span><span class="sxs-lookup"><span data-stu-id="f750a-129">For a definition of the different status values, see the listing under the *dwInternetStatus* parameter of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span>

    <span data-ttu-id="f750a-130">Приведенный ниже оператор switch представляет собой пример того, как обрабатывает обратные вызовы состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-130">The following switch statement is an example of how to handle status callbacks.</span></span>

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  <span data-ttu-id="f750a-131">Создайте код для управления значениями состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-131">Create the code to handle the status values.</span></span>

    <span data-ttu-id="f750a-132">Код для управления каждым из значений состояния зависит от предполагаемого использования функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-132">The code to handle each of the status values depends heavily on your intended use of the status callback function.</span></span> <span data-ttu-id="f750a-133">Для приложений, которые просто отслеживают ход выполнения запроса, запись строки в поле со списком может быть достаточной.</span><span class="sxs-lookup"><span data-stu-id="f750a-133">For applications that are just tracking the progress of a request, writing a string to a list box might be all you need.</span></span> <span data-ttu-id="f750a-134">Для асинхронных операций код должен поддерживать некоторые данные, возвращаемые в обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="f750a-134">For asynchronous operations, the code must handle some of the data returned in the callback.</span></span>

    <span data-ttu-id="f750a-135">Следующая функция обратного вызова состояния использует функцию Switch для определения значения Status и создает строку, включающую в себя имя значения состояния и предыдущую функцию, которая хранится в элементе Сзмемо \_ структуры контекста запроса.</span><span class="sxs-lookup"><span data-stu-id="f750a-135">The following status callback function uses a switch function to determine what the status value is and creates a string that includes the name of the status value and the previous function called, which is stored in the szMemo member of the REQUEST\_CONTEXT structure.</span></span>

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  <span data-ttu-id="f750a-136">Используйте функцию [**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) , чтобы задать функцию обратного вызова состояния для маркера [**хинтернет**](appendix-a-hinternet-handles.md) , для которого требуется получить обратные вызовы состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-136">Use the [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) function to set the status callback function on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle for which you want to receive status callbacks.</span></span>

    <span data-ttu-id="f750a-137">В следующем примере показано, как задать функцию обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="f750a-137">The following example demonstrates how to set a status callback function.</span></span>

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> <span data-ttu-id="f750a-138">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="f750a-138">WinINet does not support server implementations.</span></span> <span data-ttu-id="f750a-139">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="f750a-139">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f750a-140">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f750a-140">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f750a-141">См. также</span><span class="sxs-lookup"><span data-stu-id="f750a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f750a-142">Создание функций обратного вызова состояния</span><span class="sxs-lookup"><span data-stu-id="f750a-142">Creating Status Callback Functions</span></span>](creating-status-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="f750a-143">**интернетсетстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f750a-143">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[<span data-ttu-id="f750a-144">*интернетстатускаллбакк*</span><span class="sxs-lookup"><span data-stu-id="f750a-144">*InternetStatusCallback*</span></span>](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 