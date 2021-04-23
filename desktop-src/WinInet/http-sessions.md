---
title: HTTP-сеансы
description: Доступ к ресурсам WWW осуществляется с помощью протокола HTTP.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134099"
---
# <a name="http-sessions"></a><span data-ttu-id="0bed2-103">HTTP-сеансы</span><span class="sxs-lookup"><span data-stu-id="0bed2-103">HTTP Sessions</span></span>

<span data-ttu-id="0bed2-104">WinINet позволяет получать доступ к ресурсам в Интернете (WWW).</span><span class="sxs-lookup"><span data-stu-id="0bed2-104">WinINet enables you to access resources on the World Wide Web (WWW).</span></span> <span data-ttu-id="0bed2-105">Доступ к этим ресурсам можно получить напрямую с помощью [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (Дополнительные сведения см. в разделе [доступ к URL-адресам напрямую](handling-uniform-resource-locators.md)).</span><span class="sxs-lookup"><span data-stu-id="0bed2-105">These resources can be accessed directly by using [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for more information, see [Accessing URLs Directly](handling-uniform-resource-locators.md)).</span></span>

<span data-ttu-id="0bed2-106">Доступ к ресурсам WWW осуществляется с помощью протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="0bed2-106">Resources on the WWW are accessed by using http.</span></span> <span data-ttu-id="0bed2-107">Функции HTTP обработают базовые протоколы, позволяя приложению получать доступ к информации в Интернете.</span><span class="sxs-lookup"><span data-stu-id="0bed2-107">The HTTP functions handle the underlying protocols, while allowing your application to access information on the WWW.</span></span> <span data-ttu-id="0bed2-108">По мере развития протокола HTTP базовые протоколы обновляются для поддержки поведения функций.</span><span class="sxs-lookup"><span data-stu-id="0bed2-108">As the HTTP protocol evolves, the underlying protocols are updated to maintain function behavior.</span></span>

<span data-ttu-id="0bed2-109">На следующей диаграмме показаны связи функций, используемых с протоколом HTTP.</span><span class="sxs-lookup"><span data-stu-id="0bed2-109">The following diagram shows the relationships of the functions that are used with the HTTP protocol.</span></span> <span data-ttu-id="0bed2-110">Затененные поля представляют функции, которые возвращают дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный функцией, от которой они зависят.</span><span class="sxs-lookup"><span data-stu-id="0bed2-110">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![функции WinInet, используемые для HTTP](images/ax-wnt05.png)

<span data-ttu-id="0bed2-112">Дополнительные сведения см. в разделе [Хинтернет Handles](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="0bed2-112">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-to-access-the-www"></a><span data-ttu-id="0bed2-113">Использование функций WinINet для доступа к веб-публикации</span><span class="sxs-lookup"><span data-stu-id="0bed2-113">Using the WinINet Functions to Access the WWW</span></span>

-   [<span data-ttu-id="0bed2-114">Инициализация подключения к WWW</span><span class="sxs-lookup"><span data-stu-id="0bed2-114">Initiating a Connection to the WWW</span></span>](#initiating-a-connection-to-the-www)
-   [<span data-ttu-id="0bed2-115">Открытие запроса</span><span class="sxs-lookup"><span data-stu-id="0bed2-115">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="0bed2-116">Добавление заголовков запроса</span><span class="sxs-lookup"><span data-stu-id="0bed2-116">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="0bed2-117">Отправка запроса</span><span class="sxs-lookup"><span data-stu-id="0bed2-117">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="0bed2-118">Отправка данных на сервер</span><span class="sxs-lookup"><span data-stu-id="0bed2-118">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="0bed2-119">Получение сведений о запросе</span><span class="sxs-lookup"><span data-stu-id="0bed2-119">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="0bed2-120">Загрузка ресурсов из Интернета</span><span class="sxs-lookup"><span data-stu-id="0bed2-120">Downloading Resources from the WWW</span></span>](#downloading-resources-from-the-www)

<span data-ttu-id="0bed2-121">Следующие функции используются во время сеансов HTTP для доступа к WWW.</span><span class="sxs-lookup"><span data-stu-id="0bed2-121">The following functions are used during HTTP sessions to access the WWW.</span></span>



| <span data-ttu-id="0bed2-122">Функция</span><span class="sxs-lookup"><span data-stu-id="0bed2-122">Function</span></span>                                               | <span data-ttu-id="0bed2-123">Описание</span><span class="sxs-lookup"><span data-stu-id="0bed2-123">Description</span></span>                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bed2-124">**хттпаддрекуессеадерс**</span><span class="sxs-lookup"><span data-stu-id="0bed2-124">**HttpAddRequestHeaders**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | <span data-ttu-id="0bed2-125">Добавляет заголовки HTTP-запросов в обработчик HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="0bed2-125">Adds HTTP request headers to the HTTP request handle.</span></span> <span data-ttu-id="0bed2-126">Эта функция требует создания маркера, созданного с помощью [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="0bed2-126">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                 |
| [<span data-ttu-id="0bed2-127">**хттпопенрекуест**</span><span class="sxs-lookup"><span data-stu-id="0bed2-127">**HttpOpenRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | <span data-ttu-id="0bed2-128">Открывает обработчик HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="0bed2-128">Opens an HTTP request handle.</span></span> <span data-ttu-id="0bed2-129">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0bed2-129">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                                                         |
| [<span data-ttu-id="0bed2-130">**хттпкуеринфо**</span><span class="sxs-lookup"><span data-stu-id="0bed2-130">**HttpQueryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | <span data-ttu-id="0bed2-131">Запрашивает сведения о HTTP-запросе.</span><span class="sxs-lookup"><span data-stu-id="0bed2-131">Queries information about an HTTP request.</span></span> <span data-ttu-id="0bed2-132">Эта функция требует создания маркера, созданного функцией [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="0bed2-132">This function requires a handle created by the [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="0bed2-133">**хттпсендрекуест**</span><span class="sxs-lookup"><span data-stu-id="0bed2-133">**HttpSendRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | <span data-ttu-id="0bed2-134">Отправляет заданный HTTP-запрос на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="0bed2-134">Sends the specified HTTP request to the HTTP server.</span></span> <span data-ttu-id="0bed2-135">Эта функция требует создания маркера, созданного с помощью [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="0bed2-135">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                  |
| [<span data-ttu-id="0bed2-136">**интернетеррордлг**</span><span class="sxs-lookup"><span data-stu-id="0bed2-136">**InternetErrorDlg**</span></span>](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | <span data-ttu-id="0bed2-137">Отображает стандартные диалоговые окна для распространенных условий возникновения ошибок Интернета.</span><span class="sxs-lookup"><span data-stu-id="0bed2-137">Displays predefined dialog boxes for common Internet error conditions.</span></span> <span data-ttu-id="0bed2-138">Для этой функции требуется маркер, используемый в вызове [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="0bed2-138">This function requires the handle used in the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>                     |



 

### <a name="initiating-a-connection-to-the-www"></a><span data-ttu-id="0bed2-139">Инициализация подключения к WWW</span><span class="sxs-lookup"><span data-stu-id="0bed2-139">Initiating a Connection to the WWW</span></span>

<span data-ttu-id="0bed2-140">Чтобы запустить подключение к WWW, приложение должно вызвать функцию [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) в корневом [**хинтернет**](appendix-a-hinternet-handles.md) , возвращенном [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="0bed2-140">To start a connection to the WWW, the application must call the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function on the root [**HINTERNET**](appendix-a-hinternet-handles.md) returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="0bed2-141">[**Интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) должен установить сеанс HTTP, объявив \_ тип HTTP службы Интернета \_ .</span><span class="sxs-lookup"><span data-stu-id="0bed2-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) must establish an HTTP session by declaring the INTERNET\_SERVICE\_HTTP service type.</span></span> <span data-ttu-id="0bed2-142">Дополнительные сведения об использовании [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)см. в разделе [Использование интернетконнект](enabling-internet-functionality.md).</span><span class="sxs-lookup"><span data-stu-id="0bed2-142">For more information on using [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), see [Using InternetConnect](enabling-internet-functionality.md).</span></span>

### <a name="opening-a-request"></a><span data-ttu-id="0bed2-143">Открытие запроса</span><span class="sxs-lookup"><span data-stu-id="0bed2-143">Opening a Request</span></span>

<span data-ttu-id="0bed2-144">Функция [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) открывает HTTP-запрос и возвращает маркер [**хинтернет**](appendix-a-hinternet-handles.md) , который может использоваться другими функциями HTTP.</span><span class="sxs-lookup"><span data-stu-id="0bed2-144">The [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function opens an HTTP request and returns an [**HINTERNET**](appendix-a-hinternet-handles.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="0bed2-145">В отличие от других открытых функций (таких как [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**Интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**Хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) не отправляет запрос в Интернет при вызове.</span><span class="sxs-lookup"><span data-stu-id="0bed2-145">Unlike the other open functions (such as [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) does not send the request to the Internet when called.</span></span> <span data-ttu-id="0bed2-146">Функция [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) отправляет запрос и устанавливает подключение по сети.</span><span class="sxs-lookup"><span data-stu-id="0bed2-146">The [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) function sends the request and establishes a connection over the network.</span></span>

<span data-ttu-id="0bed2-147">[**Хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) принимает обработчик сеанса HTTP, созданный [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , и глагол HTTP, имя объекта, строку версии, источник ссылки, типы приема, флаги и значение контекста.</span><span class="sxs-lookup"><span data-stu-id="0bed2-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) takes an HTTP session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and an HTTP verb, object name, version string, referrer, accept types, flags, and context value.</span></span>

<span data-ttu-id="0bed2-148">HTTP-команда является строкой, используемой в запросе.</span><span class="sxs-lookup"><span data-stu-id="0bed2-148">The HTTP verb is a string to be used in the request.</span></span> <span data-ttu-id="0bed2-149">Распространенные глаголы HTTP, используемые в запросах, включают GET, WHERE и POST.</span><span class="sxs-lookup"><span data-stu-id="0bed2-149">Common HTTP verbs used in requests include GET, PUT, and POST.</span></span> <span data-ttu-id="0bed2-150">Если это значение равно **null**, [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) использует значение по умолчанию Get.</span><span class="sxs-lookup"><span data-stu-id="0bed2-150">If this value is set to **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uses the default value GET.</span></span>

<span data-ttu-id="0bed2-151">Имя объекта — это строка, содержащая имя указанного целевого объекта HTTP-команды.</span><span class="sxs-lookup"><span data-stu-id="0bed2-151">The object name is a string that contains the name of the specified HTTP verb's target object.</span></span> <span data-ttu-id="0bed2-152">Обычно это имя файла, исполняемый модуль или описатель поиска.</span><span class="sxs-lookup"><span data-stu-id="0bed2-152">This is generally a file name, an executable module, or a search specifier.</span></span> <span data-ttu-id="0bed2-153">Если переданное имя объекта является пустой строкой, [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ищет страницу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0bed2-153">If the object name supplied is an empty string, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) looks for the default page.</span></span>

<span data-ttu-id="0bed2-154">Строка версии должна содержать версию HTTP.</span><span class="sxs-lookup"><span data-stu-id="0bed2-154">The version string should contain the HTTP version.</span></span> <span data-ttu-id="0bed2-155">Если этот параметр имеет **значение NULL**, функция использует "HTTP/1.1".</span><span class="sxs-lookup"><span data-stu-id="0bed2-155">If this parameter is **NULL**, the function uses ""HTTP/1.1"".</span></span>

<span data-ttu-id="0bed2-156">Источник ссылки задает адрес документа, из которого было получено имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0bed2-156">The referrer specifies the address of the document from which the object name was obtained.</span></span> <span data-ttu-id="0bed2-157">Если этот параметр имеет **значение NULL**, источник ссылки не указывается.</span><span class="sxs-lookup"><span data-stu-id="0bed2-157">If this parameter is **NULL**, no referrer is specified.</span></span>

<span data-ttu-id="0bed2-158">Строка с завершающим **нулем**, которая содержит типы Accept, указывает типы содержимого, принимаемые приложением.</span><span class="sxs-lookup"><span data-stu-id="0bed2-158">The **null**-terminated string that contains the accept types indicates the content types accepted by the application.</span></span> <span data-ttu-id="0bed2-159">Установка этого параметра в **значение NULL** означает, что приложение не принимает типы содержимого.</span><span class="sxs-lookup"><span data-stu-id="0bed2-159">Setting this parameter to **NULL** indicates that no content types are accepted by the application.</span></span> <span data-ttu-id="0bed2-160">Если указана пустая строка, приложение указывает, что оно принимает только документы типа "" Text/ \* "".</span><span class="sxs-lookup"><span data-stu-id="0bed2-160">If an empty string is supplied, the application indicates it accepts only documents of type ""text/\*"".</span></span> <span data-ttu-id="0bed2-161">Значение "" Text/" \* указывает только текстовые документы, а не рисунки или другие двоичные файлы.</span><span class="sxs-lookup"><span data-stu-id="0bed2-161">The value ""text/\*"" indicates text-only documents—not pictures or other binary files.</span></span>

<span data-ttu-id="0bed2-162">Значения флагов управляют кэшированием, файлами cookie и проблемами безопасности.</span><span class="sxs-lookup"><span data-stu-id="0bed2-162">The flag values control caching, cookies, and security issues.</span></span> <span data-ttu-id="0bed2-163">Для Microsoft Network (MSN), NTLM и других типов проверки подлинности установите флаг [ \_ \_ \_ подключения](api-flags.md) "установить флаг" для Интернета.</span><span class="sxs-lookup"><span data-stu-id="0bed2-163">For Microsoft Network (MSN), NTLM, and other types of authentication, set the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag.</span></span>

<span data-ttu-id="0bed2-164">Если в вызове [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena)был установлен флаг [ \_ \_ Async Internet](api-flags.md) Flag, то для правильной асинхронной операции должно быть задано ненулевое значение контекста.</span><span class="sxs-lookup"><span data-stu-id="0bed2-164">If the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag was set in the call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), a nonzero context value should be set for proper asynchronous operation.</span></span>

<span data-ttu-id="0bed2-165">Ниже приведен пример вызова [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="0bed2-165">The following example is a sample call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a><span data-ttu-id="0bed2-166">Добавление заголовков запроса</span><span class="sxs-lookup"><span data-stu-id="0bed2-166">Adding Request Headers</span></span>

<span data-ttu-id="0bed2-167">Функция [**хттпаддрекуессеадерс**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) позволяет приложениям добавлять в первоначальный запрос один или несколько заголовков запросов.</span><span class="sxs-lookup"><span data-stu-id="0bed2-167">The [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) function enables applications to add one or more request headers to the initial request.</span></span> <span data-ttu-id="0bed2-168">Эта функция позволяет приложению добавлять в обработчик HTTP-запросов дополнительные заголовки свободного формата. Он предназначен для использования сложными приложениями, требующими точного контроля над запросом, отправленным на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="0bed2-168">This function allows an application to append additional free-format headers to the HTTP request handle; it is intended for use by sophisticated applications that require precise control over the request sent to the HTTP server.</span></span>

<span data-ttu-id="0bed2-169">[**Хттпаддрекуессеадерс**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) требуется обработчик HTTP-запроса, созданный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), строка, содержащая заголовки, длину заголовков и модификаторов.</span><span class="sxs-lookup"><span data-stu-id="0bed2-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) needs an HTTP request handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), a string that contains the headers, the length of the headers, and modifiers.</span></span>

### <a name="sending-a-request"></a><span data-ttu-id="0bed2-170">Отправка запроса</span><span class="sxs-lookup"><span data-stu-id="0bed2-170">Sending a Request</span></span>

<span data-ttu-id="0bed2-171">[**Хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) устанавливает подключение к Интернету и отправляет запрос на указанный сайт.</span><span class="sxs-lookup"><span data-stu-id="0bed2-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establishes a connection to the Internet and sends the request to the specified site.</span></span> <span data-ttu-id="0bed2-172">Для этой функции требуется обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , созданный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="0bed2-172">This function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="0bed2-173">[**Хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) также может передавать дополнительные заголовки или дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0bed2-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) can also send additional headers or optional information.</span></span> <span data-ttu-id="0bed2-174">Необязательные сведения обычно используются для операций, которые записывают сведения на сервер, такие как операции размещения и POST.</span><span class="sxs-lookup"><span data-stu-id="0bed2-174">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="0bed2-175">После того как [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) отправляет запрос, приложение может использовать функции [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)и [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) в обработчике [**HINTERNET**](appendix-a-hinternet-handles.md) , созданном [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) , для загрузки ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="0bed2-175">After [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) sends the request, the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) to download the server's resources.</span></span>

### <a name="posting-data-to-the-server"></a><span data-ttu-id="0bed2-176">Отправка данных на сервер</span><span class="sxs-lookup"><span data-stu-id="0bed2-176">Posting Data to the Server</span></span>

<span data-ttu-id="0bed2-177">Для отправки данных на сервер HTTP-команда в вызове [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) должна быть либо POST, либо помещается.</span><span class="sxs-lookup"><span data-stu-id="0bed2-177">To post data to a server, the HTTP verb in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) must be either POST or PUT.</span></span> <span data-ttu-id="0bed2-178">Адрес буфера, содержащего данные POST, должен передаваться в параметр *лпоптионал* в [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="0bed2-178">The address of the buffer that contains the POST data should then be passed to the *lpOptional* parameter in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="0bed2-179">Для параметра *двоптионалленгс* необходимо задать размер данных.</span><span class="sxs-lookup"><span data-stu-id="0bed2-179">The *dwOptionalLength* parameter should be set to the size of the data.</span></span>

<span data-ttu-id="0bed2-180">Можно также использовать функцию [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) для публикации данных в [**хинтернетном**](appendix-a-hinternet-handles.md) обработчике, отправленном с помощью [**хттпсендрекуестекс**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span><span class="sxs-lookup"><span data-stu-id="0bed2-180">You can also use the [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) function to post data on an [**HINTERNET**](appendix-a-hinternet-handles.md) handle sent using [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span></span>

### <a name="getting-information-about-a-request"></a><span data-ttu-id="0bed2-181">Получение сведений о запросе</span><span class="sxs-lookup"><span data-stu-id="0bed2-181">Getting Information About a Request</span></span>

<span data-ttu-id="0bed2-182">[**Хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) позволяет приложению получать сведения о HTTP-запросе.</span><span class="sxs-lookup"><span data-stu-id="0bed2-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="0bed2-183">Функции требуется обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , созданный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), значение информационного уровня и длина буфера.</span><span class="sxs-lookup"><span data-stu-id="0bed2-183">The function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), an information level value, and a buffer length.</span></span> <span data-ttu-id="0bed2-184">[**Хттпкуеринфо**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) также принимает буфер, в котором хранятся данные, и индекс заголовков, начинающийся с нуля, который перечисляет несколько заголовков с одним и тем же именем.</span><span class="sxs-lookup"><span data-stu-id="0bed2-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

### <a name="downloading-resources-from-the-www"></a><span data-ttu-id="0bed2-185">Загрузка ресурсов из Интернета</span><span class="sxs-lookup"><span data-stu-id="0bed2-185">Downloading Resources from the WWW</span></span>

<span data-ttu-id="0bed2-186">После открытия запроса с [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и его отправки на сервер с помощью [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)приложение может использовать функции [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)и [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) для загрузки ресурса с HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="0bed2-186">After opening a request with [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sending it to the server with [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="0bed2-187">В следующем примере загружается ресурс.</span><span class="sxs-lookup"><span data-stu-id="0bed2-187">The following example downloads a resource.</span></span> <span data-ttu-id="0bed2-188">Функция принимает маркер в текущее окно, идентификационный номер поля ввода и маркер [**хинтернет**](appendix-a-hinternet-handles.md) , созданный [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) , и отправляется [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="0bed2-188">The function accepts the handle to the current window, the identification number of an edit box, and an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="0bed2-189">Он использует [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) для определения размера ресурса, а затем загружает его с помощью [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="0bed2-189">It uses [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) to determine the size of the resource and then downloads it using [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="0bed2-190">Затем содержимое отображается в поле ввода.</span><span class="sxs-lookup"><span data-stu-id="0bed2-190">The contents are then displayed in the edit box.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="0bed2-191">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="0bed2-191">WinINet does not support server implementations.</span></span> <span data-ttu-id="0bed2-192">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="0bed2-192">In addition, it should not be used from a service.</span></span> <span data-ttu-id="0bed2-193">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="0bed2-193">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 