---
description: Службы Microsoft Windows HTTP (WinHTTP) предоставляют набор функций C/C++, позволяющих приложению получать доступ к ресурсам HTTP в Интернете. В этом разделе приводятся общие сведения о том, как эти функции используются для взаимодействия с HTTP-сервером.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Общие сведения о сеансах WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145163"
---
# <a name="winhttp-sessions-overview"></a><span data-ttu-id="6d1b7-104">Общие сведения о сеансах WinHTTP</span><span class="sxs-lookup"><span data-stu-id="6d1b7-104">WinHTTP Sessions Overview</span></span>

<span data-ttu-id="6d1b7-105">Службы Microsoft Windows HTTP (WinHTTP) предоставляют набор функций C/C++, позволяющих приложению получать доступ к ресурсам HTTP в Интернете.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-105">The Microsoft Windows HTTP Services (WinHTTP) exposes a set of C/C++ functions that enable your application to access HTTP resources on the Web.</span></span> <span data-ttu-id="6d1b7-106">В этом разделе приводятся общие сведения о том, как эти функции используются для взаимодействия с HTTP-сервером.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-106">This topic provides an overview of how these functions are used to interact with an HTTP server.</span></span>

-   [<span data-ttu-id="6d1b7-107">Использование API WinHTTP для доступа к веб-службам</span><span class="sxs-lookup"><span data-stu-id="6d1b7-107">Using the WinHTTP API to Access the Web</span></span>](#using-the-winhttp-api-to-access-the-web)
-   [<span data-ttu-id="6d1b7-108">Инициализация WinHTTP</span><span class="sxs-lookup"><span data-stu-id="6d1b7-108">Initializing WinHTTP</span></span>](#initializing-winhttp)
-   [<span data-ttu-id="6d1b7-109">Открытие запроса</span><span class="sxs-lookup"><span data-stu-id="6d1b7-109">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="6d1b7-110">Добавление заголовков запроса</span><span class="sxs-lookup"><span data-stu-id="6d1b7-110">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="6d1b7-111">Отправка запроса</span><span class="sxs-lookup"><span data-stu-id="6d1b7-111">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="6d1b7-112">Отправка данных на сервер</span><span class="sxs-lookup"><span data-stu-id="6d1b7-112">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="6d1b7-113">Получение сведений о запросе</span><span class="sxs-lookup"><span data-stu-id="6d1b7-113">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="6d1b7-114">Загрузка ресурсов из Интернета</span><span class="sxs-lookup"><span data-stu-id="6d1b7-114">Downloading Resources from the Web</span></span>](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a><span data-ttu-id="6d1b7-115">Использование API WinHTTP для доступа к веб-службам</span><span class="sxs-lookup"><span data-stu-id="6d1b7-115">Using the WinHTTP API to Access the Web</span></span>

<span data-ttu-id="6d1b7-116">На следующей схеме показан порядок, в котором функции WinHTTP обычно вызываются при взаимодействии с HTTP-сервером.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-116">The following diagram shows the order in which WinHTTP functions are typically called when interacting with an HTTP server.</span></span> <span data-ttu-id="6d1b7-117">Затененные поля представляют функции, которые создают дескриптор [хинтернет](hinternet-handles-in-winhttp.md) , а обычные поля представляют функции, использующие эти дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-117">The shaded boxes represent functions that generate an [HINTERNET](hinternet-handles-in-winhttp.md) handle, while the plain boxes represent functions that use those handles.</span></span>

![функции, создающие дескрипторы](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a><span data-ttu-id="6d1b7-119">Инициализация WinHTTP</span><span class="sxs-lookup"><span data-stu-id="6d1b7-119">Initializing WinHTTP</span></span>

<span data-ttu-id="6d1b7-120">Перед взаимодействием с сервером необходимо инициализировать WinHTTP с помощью вызова [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span><span class="sxs-lookup"><span data-stu-id="6d1b7-120">Before interacting with a server, WinHTTP must be initialized by calling [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span></span> <span data-ttu-id="6d1b7-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) создает контекст сеанса для сохранения сведений об HTTP-сеансе и возвращает маркер сеанса.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) creates a session context to maintain details about the HTTP session, and returns a session handle.</span></span> <span data-ttu-id="6d1b7-122">С помощью этого маркера функция [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) может указать целевой сервер HTTP или протокол HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-122">Using this handle, the [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) function is then able to specify a target HTTP or Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

> [!Note]  
> <span data-ttu-id="6d1b7-123">Вызов [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) не приводит к фактическому подключению к HTTP-серверу до тех пор, пока не будет выполнен запрос к определенному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-123">A call to [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) does not result in an actual connection to the HTTP server until a request is made for a specific resource.</span></span>

 

## <a name="opening-a-request"></a><span data-ttu-id="6d1b7-124">Открытие запроса</span><span class="sxs-lookup"><span data-stu-id="6d1b7-124">Opening a Request</span></span>

<span data-ttu-id="6d1b7-125">Функция [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) открывает HTTP-запрос для определенного ресурса и возвращает маркер [хинтернет](hinternet-handles-in-winhttp.md) , который может использоваться другими функциями HTTP.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-125">The [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function opens an HTTP request for a particular resource and returns an [HINTERNET](hinternet-handles-in-winhttp.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="6d1b7-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) не отправляет запрос на сервер при вызове.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) does not send the request to the server when called.</span></span> <span data-ttu-id="6d1b7-127">Функция [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) на самом деле устанавливает подключение по сети и отправляет запрос.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-127">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function actually establishes a connection over the network and sends the request.</span></span>

<span data-ttu-id="6d1b7-128">В следующем примере показан пример вызова [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , в котором используются параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-128">The following example shows a sample call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) that uses the default options.</span></span>

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a><span data-ttu-id="6d1b7-129">Добавление заголовков запроса</span><span class="sxs-lookup"><span data-stu-id="6d1b7-129">Adding Request Headers</span></span>

<span data-ttu-id="6d1b7-130">Функция [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) позволяет приложению добавлять в обработчик HTTP-запросов дополнительные заголовки запросов свободного формата.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-130">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function allows an application to append additional free-format request headers to the HTTP request handle.</span></span> <span data-ttu-id="6d1b7-131">Он предназначен для использования сложными приложениями, требующими точного контроля над запросами, отправленными на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-131">It is intended for use by sophisticated applications that require precise control over the requests sent to the HTTP server.</span></span>

<span data-ttu-id="6d1b7-132">Функции [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) требуется обработчик HTTP-запроса, созданный [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), строка, содержащая заголовки, длину заголовков и любые модификаторы.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-132">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function requires an HTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), a string that contains the headers, the length of the headers, and any modifiers.</span></span>

<span data-ttu-id="6d1b7-133">С [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)можно использовать следующие модификаторы.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-133">The following modifiers can be used with [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>



| <span data-ttu-id="6d1b7-134">Модификатор</span><span class="sxs-lookup"><span data-stu-id="6d1b7-134">Modifier</span></span>                                                                                         | <span data-ttu-id="6d1b7-135">Описание</span><span class="sxs-lookup"><span data-stu-id="6d1b7-135">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d1b7-136">**\_ \_ Добавление флага аддрек WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-136">**WINHTTP\_ADDREQ\_FLAG\_ADD**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | <span data-ttu-id="6d1b7-137">Добавляет заголовок, если он не существует.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-137">Adds the header if it does not exist.</span></span> <span data-ttu-id="6d1b7-138">Используется с [**\_ \_ флагом WinHTTP аддрек \_ Replace**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span><span class="sxs-lookup"><span data-stu-id="6d1b7-138">Used with [**WINHTTP\_ADDREQ\_FLAG\_REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="6d1b7-139">**\_флаг АДДРЕК \_ WinHTTP \_ Добавить, \_ Если \_ новый**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-139">**WINHTTP\_ADDREQ\_FLAG\_ADD\_IF\_NEW**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | <span data-ttu-id="6d1b7-140">Добавляет заголовок, только если он еще не существует; в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-140">Adds the header only if it does not already exist; otherwise, an error is returned.</span></span>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="6d1b7-141">**\_ \_ объединение флагов WinHTTP аддрек \_**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-141">**WINHTTP\_ADDREQ\_FLAG\_COALESCE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | <span data-ttu-id="6d1b7-142">Объединяет заголовки с одним и тем же именем.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-142">Merges headers of the same name.</span></span>                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="6d1b7-143">**\_ \_ объединение флага аддрек WinHTTP \_ \_ с \_ запятой**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-143">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_COMMA**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | <span data-ttu-id="6d1b7-144">Объединяет заголовки с одним и тем же именем с помощью запятой.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-144">Merges headers of the same name using a comma.</span></span> <span data-ttu-id="6d1b7-145">Например, добавление "Accept: Text/ \* " с последующим "Accept: Audio/ \* " с этим флагом образует один заголовок "Accept: Text/ \* , Audio/ \* ", что приводит к объединению первого заголовка.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-145">For example, adding "Accept: text/\*" followed by "Accept: audio/\*" with this flag forms the single header "Accept: text/\*, audio/\*", causing the first header found to be merged.</span></span> <span data-ttu-id="6d1b7-146">Для обеспечения согласованной схемы с объединенными и разделенными заголовками используется вызывающее приложение.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-146">It is up to the calling application to ensure a cohesive scheme with respect to merged/separate headers.</span></span> |
| [<span data-ttu-id="6d1b7-147">**\_ \_ объединение флагов WinHTTP аддрек \_ \_ с \_ точкой с запятой**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-147">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_SEMICOLON**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | <span data-ttu-id="6d1b7-148">Объединяет заголовки с одним и тем же именем с помощью точки с запятой.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-148">Merges headers of the same name using a semicolon.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="6d1b7-149">**\_ \_ Замена флага аддрек WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6d1b7-149">**WINHTTP\_ADDREQ\_FLAG\_REPLACE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | <span data-ttu-id="6d1b7-150">Заменяет или удаляет заголовок.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-150">Replaces or removes a header.</span></span> <span data-ttu-id="6d1b7-151">Если значение заголовка пусто и заголовок найден, он удаляется.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-151">If the header value is empty and the header is found, it is removed.</span></span> <span data-ttu-id="6d1b7-152">Если значение заголовка не пустое, значение заголовка заменяется.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-152">If the header value is not empty, the header value is replaced.</span></span>                                                                                                                                                                            |



 

## <a name="sending-a-request"></a><span data-ttu-id="6d1b7-153">Отправка запроса</span><span class="sxs-lookup"><span data-stu-id="6d1b7-153">Sending a Request</span></span>

<span data-ttu-id="6d1b7-154">Функция [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) устанавливает соединение с сервером и отправляет запрос на указанный сайт.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-154">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function establishes a connection to the server and sends the request to the specified site.</span></span> <span data-ttu-id="6d1b7-155">Для этой функции требуется обработчик [хинтернет](hinternet-handles-in-winhttp.md) , созданный [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="6d1b7-155">This function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span> <span data-ttu-id="6d1b7-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) также может передавать дополнительные заголовки или дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) can also send additional headers or optional information.</span></span> <span data-ttu-id="6d1b7-157">Необязательные сведения обычно используются для операций, которые записывают сведения на сервер, такие как операции размещения и POST.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-157">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="6d1b7-158">После того как функция [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) отправит запрос, приложение может использовать функции [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) и [**винхттпкуеридатааваилабле**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) в обработчике [хинтернет](hinternet-handles-in-winhttp.md) для загрузки ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-158">After the [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function sends the request, the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions on the [HINTERNET](hinternet-handles-in-winhttp.md) handle to download the server's resources.</span></span>

## <a name="posting-data-to-the-server"></a><span data-ttu-id="6d1b7-159">Отправка данных на сервер</span><span class="sxs-lookup"><span data-stu-id="6d1b7-159">Posting Data to the Server</span></span>

<span data-ttu-id="6d1b7-160">Для отправки данных на сервер [*HTTP-команда*](glossary.md) в вызове [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) должна быть либо POST, либо помещается.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-160">To post data to a server, the [*HTTP verb*](glossary.md) in the call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) must be either POST or PUT.</span></span> <span data-ttu-id="6d1b7-161">При вызове [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) параметр *двтоталленгс* должен быть установлен равным размеру данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-161">When [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) is called, the *dwTotalLength* parameter should be set to the size of the data in bytes.</span></span> <span data-ttu-id="6d1b7-162">Затем используйте [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) для передачи данных на сервер.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-162">Then use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) to post the data to the server.</span></span>

<span data-ttu-id="6d1b7-163">Кроме того, можно присвоить параметру *Лпоптионал* [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) адрес буфера, содержащего данные, которые должны быть отправлены на сервер.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-163">Alternatively, set the *lpOptional* parameter of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to the address of a buffer that contains data to post to the server.</span></span> <span data-ttu-id="6d1b7-164">При использовании этого метода необходимо установить оба параметра *двоптионалленгс* и *двтоталленгс* в [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) в качестве размера публикуемых данных.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-164">When using this technique, you must set both the *dwOptionalLength* and *dwTotalLength* parameters of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to be the size of the data being posted.</span></span> <span data-ttu-id="6d1b7-165">Вызов [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) таким образом устраняет необходимость вызова [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span><span class="sxs-lookup"><span data-stu-id="6d1b7-165">Calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in this manner eliminates the need to call [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span></span>

## <a name="getting-information-about-a-request"></a><span data-ttu-id="6d1b7-166">Получение сведений о запросе</span><span class="sxs-lookup"><span data-stu-id="6d1b7-166">Getting Information About a Request</span></span>

<span data-ttu-id="6d1b7-167">Функция [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) позволяет приложению получать сведения о HTTP-запросе.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-167">The [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="6d1b7-168">Функции требуется обработчик [хинтернет](hinternet-handles-in-winhttp.md) , созданный [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), значение информационного уровня и длина буфера.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-168">The function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), an information level value, and a buffer length.</span></span> <span data-ttu-id="6d1b7-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) также принимает буфер, в котором хранятся данные, и индекс заголовков, начинающийся с нуля, который перечисляет несколько заголовков с одним и тем же именем.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

<span data-ttu-id="6d1b7-170">Используйте любое из значений уровня информации на странице « [**Флаги сведений о запросе**](query-info-flags.md) » с модификатором для управления форматом, в котором данные хранятся в параметре *лпвбуффер* [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="6d1b7-170">Use any of the information level values found on the [**Query Info Flags**](query-info-flags.md) page with a modifier to control the format in which the information is stored in the *lpvBuffer* parameter of [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

## <a name="downloading-resources-from-the-web"></a><span data-ttu-id="6d1b7-171">Загрузка ресурсов из Интернета</span><span class="sxs-lookup"><span data-stu-id="6d1b7-171">Downloading Resources from the Web</span></span>

<span data-ttu-id="6d1b7-172">После открытия запроса с помощью функции [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , отправки ее на сервер с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)и подготовки обработчика запросов к получению ответа с помощью [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), приложение может использовать функции [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) и [**винхттпкуеридатааваилабле**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) для загрузки ресурса с HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-172">After opening a request with the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function, sending it to the server with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), and preparing the request handle to receive a response with [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="6d1b7-173">В следующем примере кода показано, как скачать ресурс с семантикой защищенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-173">The following sample code shows how to download a resource with secure transaction semantics.</span></span> <span data-ttu-id="6d1b7-174">В примере кода инициализируется программный интерфейс (API) WinHTTP, выбирается целевой HTTPS-сервер, а затем открывается и отправляется запрос для этого защищенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-174">The sample code initializes the WinHTTP application programming interface (API), selects a target HTTPS server, and then opens and sends a request for this secure resource.</span></span> <span data-ttu-id="6d1b7-175">[**Винхттпкуеридатааваилабле**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) используется с обработчиком запросов для определения объема данных, доступных для загрузки, а затем для считывания этих данных используется [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) .</span><span class="sxs-lookup"><span data-stu-id="6d1b7-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) is used with the request handle to determine how much data is available for download, and then [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) is used to read that data.</span></span> <span data-ttu-id="6d1b7-176">Этот процесс повторяется до тех пор, пока не будет получен и отображен весь документ.</span><span class="sxs-lookup"><span data-stu-id="6d1b7-176">This process is repeated until the entire document has been retrieved and displayed.</span></span>


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



