---
title: Файлы cookie HTTP
description: Файлы cookie HTTP предоставляют серверу механизм для хранения и извлечения сведений о состоянии в системе клиентского приложения.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700883"
---
# <a name="http-cookies"></a><span data-ttu-id="cf9b8-103">Файлы cookie HTTP</span><span class="sxs-lookup"><span data-stu-id="cf9b8-103">HTTP Cookies</span></span>

<span data-ttu-id="cf9b8-104">Файлы cookie HTTP предоставляют серверу механизм для хранения и извлечения сведений о состоянии в системе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-104">HTTP cookies provide the server with a mechanism to store and retrieve state information on the client application's system.</span></span> <span data-ttu-id="cf9b8-105">Этот механизм позволяет веб-приложениям сохранять сведения о выбранных элементах, предпочтениях пользователей, сведения о регистрации и другие сведения, которые можно получить позже.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-105">This mechanism allows web-based applications the ability to store information about selected items, user preferences, registration information, and other information that can be retrieved later.</span></span>

## <a name="cookie-related-headers"></a><span data-ttu-id="cf9b8-106">Заголовки Cookie-Related</span><span class="sxs-lookup"><span data-stu-id="cf9b8-106">Cookie-Related Headers</span></span>

<span data-ttu-id="cf9b8-107">Есть два заголовка: Set-Cookie и cookie, связанные с файлами cookie.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-107">There are two headers, Set-Cookie and Cookie, that are related to cookies.</span></span> <span data-ttu-id="cf9b8-108">Заголовок Set-Cookie отправляется сервером в ответ на HTTP-запрос, который используется для создания файла cookie в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-108">The Set-Cookie header is sent by the server in response to an HTTP request, which is used to create a cookie on the user's system.</span></span> <span data-ttu-id="cf9b8-109">Заголовок Cookie включается клиентским приложением с HTTP-запросом, отправленным на сервер, если имеется файл cookie с совпадающим доменом и путем.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-109">The Cookie header is included by the client application with an HTTP request sent to a server, if there is a cookie that has a matching domain and path.</span></span>

### <a name="set-cookie-header"></a><span data-ttu-id="cf9b8-110">Заголовок Set-Cookie</span><span class="sxs-lookup"><span data-stu-id="cf9b8-110">Set-Cookie Header</span></span>

<span data-ttu-id="cf9b8-111">Заголовок ответа Set-Cookie использует следующий формат:</span><span class="sxs-lookup"><span data-stu-id="cf9b8-111">The Set-Cookie response header uses the following format:</span></span>

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

<span data-ttu-id="cf9b8-112">Одна или несколько строк строки (разделенных точкой с запятой), которые следуют за значением *имени* шаблона, =  должны быть добавлены в заголовок ответа Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-112">One or more string sequences (separated by semicolons) that follow the pattern *name*=*value* must be included in the Set-Cookie response header.</span></span> <span data-ttu-id="cf9b8-113">Сервер может использовать эти последовательности строк для хранения данных в системе клиента.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-113">The server can use these string sequences to store data on the client's system.</span></span>

<span data-ttu-id="cf9b8-114">Дата истечения срока действия задается в формате срок действия =*Дата*, где *Дата* — Дата истечения срока действия по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="cf9b8-114">The expiration date is set by using the format expires=*date*, where *date* is the expiration date in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="cf9b8-115">Если дата окончания срока действия не задана, то срок действия файла cookie истекает после завершения сеанса Интернета.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-115">If the expiration date is not set, the cookie expires after the Internet session ends.</span></span> <span data-ttu-id="cf9b8-116">В противном случае файл cookie сохраняется в кэше до даты окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-116">Otherwise, the cookie is persisted in the cache until the expiration date.</span></span> <span data-ttu-id="cf9b8-117">Дата должна иметь следующий формат:</span><span class="sxs-lookup"><span data-stu-id="cf9b8-117">The date must use the following format:</span></span>

<span data-ttu-id="cf9b8-118">*день*, *дд* - *МММ* - *гггг* *чч*:*мм*:*СС* GMT</span><span class="sxs-lookup"><span data-stu-id="cf9b8-118">*DAY*, *DD*-*MMM*-*YYYY* *HH*:*MM*:*SS* GMT</span></span>

<dl> <dt>

<span data-ttu-id="cf9b8-119"><span id="DAY"></span><span id="day"></span>*Ежедневные*</span><span class="sxs-lookup"><span data-stu-id="cf9b8-119"><span id="DAY"></span><span id="day"></span>*DAY*</span></span>
</dt> <dd>

<span data-ttu-id="cf9b8-120">День недели (Sun, Пн, вторник, среда, четверг, пятница, Кот).</span><span class="sxs-lookup"><span data-stu-id="cf9b8-120">The day of the week (Sun, Mon, Tue, Wed, Thu, Fri, Sat).</span></span>

</dd> <dt>

<span data-ttu-id="cf9b8-121"><span id="DD"></span><span id="dd"></span>*DDL*</span><span class="sxs-lookup"><span data-stu-id="cf9b8-121"><span id="DD"></span><span id="dd"></span>*DD*</span></span>
</dt> <dd>

<span data-ttu-id="cf9b8-122">День месяца (например, 01 для первого дня месяца).</span><span class="sxs-lookup"><span data-stu-id="cf9b8-122">The day in the month (such as 01 for the first day of the month).</span></span>

</dd> <dt>

<span data-ttu-id="cf9b8-123"><span id="MMM"></span><span id="mmm"></span>*МСЕК*</span><span class="sxs-lookup"><span data-stu-id="cf9b8-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span></span>
</dt> <dd>

<span data-ttu-id="cf9b8-124">Аббревиатура из трех букв для месяца (Jan, фев, Mar, Апр, Май, июн, Июл, Авг, Sep, Oct, ноя, дек).</span><span class="sxs-lookup"><span data-stu-id="cf9b8-124">The three-letter abbreviation for the month (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).</span></span>

</dd> <dt>

<span data-ttu-id="cf9b8-125"><span id="YYYY"></span><span id="yyyy"></span>*ГГГГ*</span><span class="sxs-lookup"><span data-stu-id="cf9b8-125"><span id="YYYY"></span><span id="yyyy"></span>*YYYY*</span></span>
</dt> <dd>

<span data-ttu-id="cf9b8-126">Год.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-126">The year.</span></span>

</dd> <dt>

<span data-ttu-id="cf9b8-127"><span id="HH"></span><span id="hh"></span>*ФОРМАТЕ*</span><span class="sxs-lookup"><span data-stu-id="cf9b8-127"><span id="HH"></span><span id="hh"></span>*HH*</span></span>
</dt> <dd>

<span data-ttu-id="cf9b8-128">Значение часа в воинское время (например, 22-10:00 P.M.).</span><span class="sxs-lookup"><span data-stu-id="cf9b8-128">The hour value in military time (22 would be 10:00 P.M., for example).</span></span>

</dd> <dt>

<span data-ttu-id="cf9b8-129"><span id="MM"></span><span id="mm"></span>*ММ*</span><span class="sxs-lookup"><span data-stu-id="cf9b8-129"><span id="MM"></span><span id="mm"></span>*MM*</span></span>
</dt> <dd>

<span data-ttu-id="cf9b8-130">Значение минуты.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-130">The minute value.</span></span>

</dd> <dt>

<span data-ttu-id="cf9b8-131"><span id="SS"></span><span id="ss"></span>*НН*</span><span class="sxs-lookup"><span data-stu-id="cf9b8-131"><span id="SS"></span><span id="ss"></span>*SS*</span></span>
</dt> <dd>

<span data-ttu-id="cf9b8-132">Второе значение в вычитании.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-132">The second value.</span></span>

</dd> </dl>

<span data-ttu-id="cf9b8-133">Указание доменного имени с помощью шаблона домен =*доменное \_ имя* является необязательным для постоянных файлов cookie и используется для обозначения конца домена, для которого действителен файл cookie.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-133">Specifying the domain name, using the pattern domain=*domain\_name*, is optional for persistent cookies and is used to indicate the end of the domain for which the cookie is valid.</span></span> <span data-ttu-id="cf9b8-134">Файлы cookie сеанса, указывающие домен, отклоняются.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-134">Session cookies that specify a domain are rejected.</span></span> <span data-ttu-id="cf9b8-135">Если указанное окончание доменного имени совпадает с запросом, файл cookie пытается сопоставить путь, чтобы определить, следует ли отправлять файл cookie.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-135">If the specified domain name ending matches the request, the cookie tries to match the path to determine if the cookie should be sent.</span></span> <span data-ttu-id="cf9b8-136">Например, если доменное имя заканчивается на. microsoft.com, будут проверены запросы к home.microsoft.com и support.microsoft.com, чтобы увидеть, соответствует ли указанный шаблон запросу.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-136">For example, if the domain name ending is .microsoft.com, requests to home.microsoft.com and support.microsoft.com would be checked to see if the specified pattern matches the request.</span></span> <span data-ttu-id="cf9b8-137">Имя домена должно содержать по крайней мере два или три периода, чтобы запретить установку файлов cookie для широко используемых конечных имен доменов, таких как. com,. edu и co.jp.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-137">The domain name must have at least two or three periods in it to prevent cookies from being set for widely used domain name endings, such as .com, .edu, and co.jp.</span></span> <span data-ttu-id="cf9b8-138">Допустимые доменные имена будут похожи на. microsoft.com,. someschool.edu и. someserver.co.jp.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-138">Allowable domain names would be similar to .microsoft.com, .someschool.edu, and .someserver.co.jp.</span></span> <span data-ttu-id="cf9b8-139">Только узлы в указанном домене могут устанавливать файл cookie для домена.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-139">Only hosts within the specified domain can set a cookie for a domain.</span></span>

<span data-ttu-id="cf9b8-140">Задание пути с использованием шаблона Path =*часть \_ path* является необязательным и может использоваться для указания подмножества URL-адресов, для которых действителен файл cookie.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-140">Setting the path, using the pattern path=*some\_path*, is optional and can be used to specify a subset of the URLs for which the cookie is valid.</span></span> <span data-ttu-id="cf9b8-141">Если указан путь, то файл cookie считается допустимым для всех запросов, соответствующих этому пути.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-141">If a path is specified, the cookie is considered valid for any requests that match that path.</span></span> <span data-ttu-id="cf9b8-142">Например, если указан путь/ексампле, то запросы с путями/ексамплекоде и code.htm/ексампле/будут совпадать.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-142">For example, if the specified path is /example, requests with the paths /examplecode and /example/code.htm would match.</span></span> <span data-ttu-id="cf9b8-143">Если путь не указан, предполагается, что путь является путем к ресурсу, связанному с заголовком Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-143">If no path is specified, the path is assumed to be the path of the resource associated with the Set-Cookie header.</span></span>

<span data-ttu-id="cf9b8-144">Файл cookie также может быть помечен как безопасный, что указывает, что файл cookie может быть отправлен только на HTTPS-серверы.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-144">The cookie can also be marked as secure, which specifies that the cookie can be sent only to https servers.</span></span>

<span data-ttu-id="cf9b8-145">Наконец, файл cookie можно пометить как HttpOnly (атрибуты не учитывают регистр), чтобы указать, что файл cookie не является сценарным и не должен быть отображен клиентскому приложению по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-145">Finally, a cookie can be marked as HttpOnly (attributes are not case-sensitive), to indicate that the cookie is non-scriptable and should not be revealed to the client application, for security reasons.</span></span> <span data-ttu-id="cf9b8-146">В Windows Internet это означает, что файл cookie нельзя получить с помощью функции **интернетжеткукие** .</span><span class="sxs-lookup"><span data-stu-id="cf9b8-146">Within Windows Internet, this means that the cookie cannot be retrieved through the **InternetGetCookie** function.</span></span>

### <a name="cookie-header"></a><span data-ttu-id="cf9b8-147">Заголовок файла cookie</span><span class="sxs-lookup"><span data-stu-id="cf9b8-147">Cookie Header</span></span>

<span data-ttu-id="cf9b8-148">Заголовок Cookie включается в любые HTTP-запросы, имеющие файл cookie, домен и путь которого соответствуют запросу.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-148">The Cookie header is included with any HTTP requests that have a cookie whose domain and path match the request.</span></span> <span data-ttu-id="cf9b8-149">Заголовок Cookie имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="cf9b8-149">The Cookie header has the following format:</span></span>

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

<span data-ttu-id="cf9b8-150">Одна или несколько строковых последовательностей, использующих  = *значение* имени формата, содержат сведения, заданные в файле cookie.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-150">One or more string sequences, using the format *name*=*value*, contain the information that was set in the cookie.</span></span>

## <a name="generating-cookies"></a><span data-ttu-id="cf9b8-151">Создание файлов cookie</span><span class="sxs-lookup"><span data-stu-id="cf9b8-151">Generating Cookies</span></span>

<span data-ttu-id="cf9b8-152">Существует три метода создания файлов cookie для Microsoft Internet Explorer: с помощью Microsoft JScript, с помощью функций WinINet и сценария CGI.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-152">There are three methods for generating cookies for Microsoft Internet Explorer: using Microsoft JScript, using the WinINet functions, and using a CGI script.</span></span> <span data-ttu-id="cf9b8-153">Все методы должны задавать сведения, включенные в заголовок Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-153">All of the methods need to set the information that is included in the Set-Cookie header.</span></span>

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a><span data-ttu-id="cf9b8-154">Создание файла cookie с помощью объектной модели DHTML</span><span class="sxs-lookup"><span data-stu-id="cf9b8-154">Generating a Cookie Using the DHTML Object Model</span></span>

<span data-ttu-id="cf9b8-155">С помощью объектной модели Dynamic HTML (DHTML) можно задать файлы cookie, вызвав свойство **cookie** объекта документа, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-155">Using the Dynamic HTML (DHTML) object model, cookies can be set by calling the **cookie** property of the document object, as shown in the following example.</span></span>

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a><span data-ttu-id="cf9b8-156">Создание файла cookie с помощью функций WinInet</span><span class="sxs-lookup"><span data-stu-id="cf9b8-156">Generating a Cookie Using the WinInet Functions</span></span>

<span data-ttu-id="cf9b8-157">Файлы cookie могут создаваться приложениями с помощью функции [**интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) .</span><span class="sxs-lookup"><span data-stu-id="cf9b8-157">Cookies can be created by applications using the [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) function.</span></span> <span data-ttu-id="cf9b8-158">Дополнительные сведения см. [в разделе Задание файла cookie](managing-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="cf9b8-158">For more information, see [Setting a Cookie](managing-cookies.md).</span></span>

### <a name="generating-a-cookie-using-a-cgi-script"></a><span data-ttu-id="cf9b8-159">Создание файла cookie с помощью сценария CGI</span><span class="sxs-lookup"><span data-stu-id="cf9b8-159">Generating a Cookie Using a CGI Script</span></span>

<span data-ttu-id="cf9b8-160">Файлы cookie создаются путем включения заголовка Set-Cookie в составе сценария CGI, входящего в HTTP-ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-160">Cookies are generated by including a Set-Cookie header as part of a CGI script included in the HTTP response to a request.</span></span>

<span data-ttu-id="cf9b8-161">В следующем примере показан сценарий CGI, который включает заголовок Set-Cookie с помощью Perl.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-161">The following example is a CGI script that includes a Set-Cookie header using Perl.</span></span>

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> <span data-ttu-id="cf9b8-162">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="cf9b8-163">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="cf9b8-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="cf9b8-164">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="cf9b8-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 