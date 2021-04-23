---
title: Получение заголовков HTTP
description: В этом учебнике описывается получение сведений о заголовках из HTTP-запросов.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b31043940b8c2127d1cfa1696d2821641d0784
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654335"
---
# <a name="retrieving-http-headers"></a><span data-ttu-id="f3657-103">Получение заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="f3657-103">Retrieving HTTP Headers</span></span>

<span data-ttu-id="f3657-104">В этом учебнике описывается получение сведений о заголовках из HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="f3657-104">This tutorial describes how to retrieve header information from HTTP requests.</span></span>

## <a name="implementation-steps"></a><span data-ttu-id="f3657-105">Шаги реализации</span><span class="sxs-lookup"><span data-stu-id="f3657-105">Implementation Steps</span></span>

<span data-ttu-id="f3657-106">Получить сведения о заголовке можно двумя способами:</span><span class="sxs-lookup"><span data-stu-id="f3657-106">There are two ways to retrieve the header information:</span></span>

-   <span data-ttu-id="f3657-107">Используйте одну из констант [**флагов сведений о запросе**](query-info-flags.md) , связанных с заголовком HTTP, которое требуется вашему приложению.</span><span class="sxs-lookup"><span data-stu-id="f3657-107">Use one of the [**Query Info Flag**](query-info-flags.md) constants associated with the HTTP header that your application needs.</span></span>
-   <span data-ttu-id="f3657-108">Используйте \_ \_ флаг настраиваемого атрибута http-запроса и передайте имя HTTP-заголовка.</span><span class="sxs-lookup"><span data-stu-id="f3657-108">Use the HTTP\_QUERY\_CUSTOM attribute flag and pass the name of the HTTP header.</span></span>

<span data-ttu-id="f3657-109">Использование константы, связанной с заголовком HTTP, которую требуется вашему приложению, выполняется быстрее, но могут существовать заголовки HTTP, с которыми не связана константа.</span><span class="sxs-lookup"><span data-stu-id="f3657-109">Using the constant associated with the HTTP header that your application needs is faster internally, but there might be HTTP headers that do not have a constant associated with them.</span></span> <span data-ttu-id="f3657-110">В таких случаях доступен метод, использующий \_ \_ флаг настраиваемого атрибута http-запроса.</span><span class="sxs-lookup"><span data-stu-id="f3657-110">For those cases, the method using the HTTP\_QUERY\_CUSTOM attribute flag is available.</span></span>

<span data-ttu-id="f3657-111">Оба метода используют функцию [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f3657-111">Both methods use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function.</span></span> <span data-ttu-id="f3657-112">[**Хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) принимает маркер [**хинтернет**](appendix-a-hinternet-handles.md) , на котором был сделан HTTP-запрос, один атрибут, буфер, значение DWORD, содержащее размер буфера, и значение индекса.</span><span class="sxs-lookup"><span data-stu-id="f3657-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle on which the HTTP request was made, one attribute, a buffer, a DWORD value that contains the buffer size, and an index value.</span></span> <span data-ttu-id="f3657-113">Модификатор можно также добавить к атрибуту, переданному в [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) , чтобы указать, в каком формате должны возвращаться данные.</span><span class="sxs-lookup"><span data-stu-id="f3657-113">A modifier can also be added to the attribute passed to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to indicate in what format the data should be returned.</span></span>

### <a name="retrieving-headers-using-a-constant"></a><span data-ttu-id="f3657-114">Получение заголовков с помощью константы</span><span class="sxs-lookup"><span data-stu-id="f3657-114">Retrieving Headers Using a Constant</span></span>

<span data-ttu-id="f3657-115">Чтобы использовать функцию [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) для получения заголовка HTTP с помощью константы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f3657-115">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using a constant, follow these steps:</span></span>

1.  <span data-ttu-id="f3657-116">Вызовите [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) с константой из списка [**Attributes**](query-info-flags.md) , **пустым** буфером и переменной, содержащей размер буфера, равным нулю.</span><span class="sxs-lookup"><span data-stu-id="f3657-116">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with a constant from the [**Attributes**](query-info-flags.md) list, a **NULL** buffer, and the variable that holds the buffer size set to zero.</span></span> <span data-ttu-id="f3657-117">Кроме того, если приложению требуются данные в определенном формате, можно добавить константу из списка [**модификаторов**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="f3657-117">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
2.  <span data-ttu-id="f3657-118">Если запрошенный заголовок HTTP существует, вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) должен завершиться ошибкой, аргумент [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) должен возвращать ошибку, \_ недостаточную \_ для буфера, а переменная, передаваемая для параметра *лпдвбуфферленгс* , должна быть установлена в соответствии с требуемым числом байтов.</span><span class="sxs-lookup"><span data-stu-id="f3657-118">If the requested HTTP header exists, the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) should fail, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) should return ERROR\_INSUFFICIENT\_BUFFER, and the variable passed for the *lpdwBufferLength* parameter should be set to the number of bytes required.</span></span>
3.  <span data-ttu-id="f3657-119">Выделение буфера с требуемым числом байтов.</span><span class="sxs-lookup"><span data-stu-id="f3657-119">Allocate a buffer with the number of bytes required.</span></span>
4.  <span data-ttu-id="f3657-120">Повторите вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="f3657-120">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="f3657-121">В следующем примере демонстрируется вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) с помощью \_ \_ необработанных \_ заголовков HTTP-запроса \_ , который представляет собой специальное значение, запрашивающее все возвращенные заголовки HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3657-121">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_RAW\_HEADERS\_CRLF constant, which is a special value that requests all of the returned HTTP headers.</span></span>


```C++
// Retrieving Headers Using a Constant
BOOL SampleCodeOne(HINTERNET hHttp)
{
   LPVOID lpOutBuffer=NULL;
   DWORD dwSize = 0;

retry:

   // This call will fail on the first pass, because
   // no buffer is allocated.
   if(!HttpQueryInfo(hHttp,HTTP_QUERY_RAW_HEADERS_CRLF,
      (LPVOID)lpOutBuffer,&dwSize,NULL))
   {
      if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
      {
         // Code to handle the case where the header isn't available.
         return TRUE;
      }
      else
      {
        // Check for an insufficient buffer.
        if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
        {
            // Allocate the necessary buffer.
            lpOutBuffer = new char[dwSize];

            // Retry the call.
            goto retry;
        }
        else
        {
            // Error handling code.
            if (lpOutBuffer)
            {
               delete [] lpOutBuffer;
            }
            return FALSE;
        }
      }
   }

   if (lpOutBuffer)
   {
      delete [] lpOutBuffer;
   }

   return TRUE;
}
```



### <a name="retrieving-headers-using-http_query_custom"></a><span data-ttu-id="f3657-122">Получение заголовков с помощью пользовательского HTTP- \_ запроса \_</span><span class="sxs-lookup"><span data-stu-id="f3657-122">Retrieving Headers Using HTTP\_QUERY\_CUSTOM</span></span>

<span data-ttu-id="f3657-123">Чтобы использовать функцию [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) для получения заголовка HTTP с помощью HTTP- \_ запроса \_ Custom, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f3657-123">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using HTTP\_QUERY\_CUSTOM, follow these steps:</span></span>

1.  <span data-ttu-id="f3657-124">Выделите буфер, достаточно большой для хранения строкового имени заголовка HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3657-124">Allocate a buffer that is large enough to hold the string name of the HTTP header.</span></span>
2.  <span data-ttu-id="f3657-125">Запишите строковое имя заголовка HTTP в буфер.</span><span class="sxs-lookup"><span data-stu-id="f3657-125">Write the string name of the HTTP header into the buffer.</span></span>
3.  <span data-ttu-id="f3657-126">Вызовите [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) с HTTP- \_ запросом \_ Custom, буфер, содержащий строковое имя заголовка HTTP, и переменную, которая содержит размер буфера.</span><span class="sxs-lookup"><span data-stu-id="f3657-126">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with HTTP\_QUERY\_CUSTOM, the buffer that contains the string name of the HTTP header, and the variable that holds the buffer size.</span></span> <span data-ttu-id="f3657-127">Кроме того, если приложению требуются данные в определенном формате, можно добавить константу из списка [**модификаторов**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="f3657-127">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
4.  <span data-ttu-id="f3657-128">Если вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) завершается ошибкой и [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку \_ недостаточно \_ буфера, перераспределите буфер с требуемым числом байтов.</span><span class="sxs-lookup"><span data-stu-id="f3657-128">If the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, reallocate a buffer with the number of bytes required.</span></span>
5.  <span data-ttu-id="f3657-129">Снова введите строковое имя заголовка HTTP в буфер.</span><span class="sxs-lookup"><span data-stu-id="f3657-129">Write the string name of the HTTP header into the buffer again.</span></span>
6.  <span data-ttu-id="f3657-130">Повторите вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="f3657-130">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="f3657-131">В следующем примере демонстрируется вызов [**хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) с использованием \_ \_ пользовательской константы HTTP-запроса для запроса заголовка HTTP Content-Type.</span><span class="sxs-lookup"><span data-stu-id="f3657-131">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_CUSTOM constant to request the Content-Type HTTP header.</span></span>


```C++
// Retrieving Headers Using HTTP_QUERY_CUSTOM
BOOL SampleCodeTwo(HINTERNET hHttp)
{
    DWORD dwSize = 20;
    LPVOID lpOutBuffer = new char[dwSize];

    StringCchPrintfA((LPSTR)lpOutBuffer,dwSize,"Content-Type");

retry:

    if(!HttpQueryInfo(hHttp,HTTP_QUERY_CUSTOM,
        (LPVOID)lpOutBuffer,&dwSize,NULL))
    {
        if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
        {
            // Code to handle the case where the header isn't available.
            delete [] lpOutBuffer;
            return TRUE;
        }
        else
        {
            // Check for an insufficient buffer.
            if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
            {
                // Allocate the necessary buffer.
                delete [] lpOutBuffer;
                lpOutBuffer = new char[dwSize];

                // Rewrite the header name in the buffer.
                StringCchPrintfA((LPSTR)lpOutBuffer,
                                 dwSize,"Content-Type");

                // Retry the call.
                goto retry;
            }
            else
            {
                // Error handling code.
                delete [] lpOutBuffer;
                return FALSE;
            }
        }
    }

   return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="f3657-132">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="f3657-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="f3657-133">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="f3657-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f3657-134">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f3657-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 