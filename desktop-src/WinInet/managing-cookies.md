---
title: Управление файлами cookie
description: В протоколе HTTP сервер или скрипт использует файлы cookie для сохранения сведений о состоянии на клиентской рабочей станции.
ms.assetid: c00279cf-9cdc-4caf-8549-af1851edfa25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0418442e961f6f4d3d2bcddb2c607ac9cf7928
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654329"
---
# <a name="managing-cookies"></a><span data-ttu-id="0429a-103">Управление файлами cookie</span><span class="sxs-lookup"><span data-stu-id="0429a-103">Managing Cookies</span></span>

<span data-ttu-id="0429a-104">В протоколе HTTP сервер или скрипт использует файлы cookie для сохранения сведений о состоянии на клиентской рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="0429a-104">Under the http protocol, a server or a script uses cookies to maintain state information on the client workstation.</span></span> <span data-ttu-id="0429a-105">Для этой цели функции WinINet реализовали постоянную базу данных cookie.</span><span class="sxs-lookup"><span data-stu-id="0429a-105">The WinINet functions have implemented a persistent cookie database for this purpose.</span></span> <span data-ttu-id="0429a-106">Их можно использовать для задания файлов cookie в и доступа к файлам cookie из базы данных cookie.</span><span class="sxs-lookup"><span data-stu-id="0429a-106">They can be used to set cookies in and access cookies from the cookie database.</span></span> <span data-ttu-id="0429a-107">Дополнительные сведения см. в разделе [файлы cookie HTTP](http-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="0429a-107">For more information, see [HTTP Cookies](http-cookies.md).</span></span>

<span data-ttu-id="0429a-108">Для управления файлами cookie можно использовать функции [**интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) и [**интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) .</span><span class="sxs-lookup"><span data-stu-id="0429a-108">The [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) and [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) functions can be used to manage cookies.</span></span>

## <a name="using-cookie-functions"></a><span data-ttu-id="0429a-109">Использование функций cookie</span><span class="sxs-lookup"><span data-stu-id="0429a-109">Using Cookie Functions</span></span>

<span data-ttu-id="0429a-110">Следующие функции позволяют приложению создавать или извлекать файлы cookie в базе данных cookie.</span><span class="sxs-lookup"><span data-stu-id="0429a-110">The following functions allow an application to create or retrieve cookies in the cookie database.</span></span>



| <span data-ttu-id="0429a-111">Функция</span><span class="sxs-lookup"><span data-stu-id="0429a-111">Function</span></span>                                       | <span data-ttu-id="0429a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0429a-112">Description</span></span>                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="0429a-113">**интернетжеткукие**</span><span class="sxs-lookup"><span data-stu-id="0429a-113">**InternetGetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) | <span data-ttu-id="0429a-114">Извлекает файлы cookie для указанного URL-адреса и всех его родительских URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="0429a-114">Retrieves cookies for the specified URL and all its parent URLs.</span></span> |
| [<span data-ttu-id="0429a-115">**интернетсеткукие**</span><span class="sxs-lookup"><span data-stu-id="0429a-115">**InternetSetCookie**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) | <span data-ttu-id="0429a-116">Задает файл cookie по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="0429a-116">Sets a cookie on the specified URL.</span></span>                              |



 

<span data-ttu-id="0429a-117">Обратите внимание, что эти функции не нуждаются в вызове [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="0429a-117">Note that these functions do not require a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="0429a-118">Файлы cookie с датой окончания срока действия хранятся в учетной записи Local Users в \\ каталоге Users "Username" \\ AppData \\ роуминг \\ Microsoft \\ Windows \\ cookies и Users " \\ username" \\ AppData \\ роуминг \\ Microsoft \\ Windows \\ cookies \\ Low Directory для приложений, работающих с низкими привилегиями.</span><span class="sxs-lookup"><span data-stu-id="0429a-118">Cookies that have an expiration date are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span> <span data-ttu-id="0429a-119">Файлы cookie, не имеющие даты окончания срока действия, хранятся в памяти и доступны только процессу, в котором они были созданы.</span><span class="sxs-lookup"><span data-stu-id="0429a-119">Cookies that do not have an expiration date are stored in memory and are available only to the process in which they were created.</span></span>

<span data-ttu-id="0429a-120">Как указано в разделе [cookies HTTP](http-cookies.md) , функция [**интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) не возвращает файлы cookie, помеченные сервером как несценарии с атрибутом HttpOnly в заголовке Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="0429a-120">As noted in the [HTTP Cookies](http-cookies.md) topic, the [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) function does not return cookies that have been marked by the server as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.</span></span>

### <a name="getting-a-cookie"></a><span data-ttu-id="0429a-121">Получение файла cookie</span><span class="sxs-lookup"><span data-stu-id="0429a-121">Getting a Cookie</span></span>

<span data-ttu-id="0429a-122">[**Интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) возвращает файлы cookie для указанного URL-адреса и всех его родительских URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="0429a-122">[**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea) returns the cookies for the specified URL and all its parent URLs.</span></span>

<span data-ttu-id="0429a-123">В следующем примере демонстрируется вызов [**интернетжеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span><span class="sxs-lookup"><span data-stu-id="0429a-123">The following example demonstrates a call to [**InternetGetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetgetcookiea).</span></span>


```C++
TCHAR szURL[256];         // buffer to hold the URL
LPTSTR lpszData = NULL;   // buffer to hold the cookie data
DWORD dwSize=0;           // variable to get the buffer size needed

// Insert code to retrieve the URL.

retry:

// The first call to InternetGetCookie will get the required
// buffer size needed to download the cookie data.
if (!InternetGetCookie(szURL, NULL, lpszData, &dwSize))
{
    // Check for an insufficient buffer error.
    if (GetLastError()== ERROR_INSUFFICIENT_BUFFER)
    {
        // Allocate the necessary buffer.
        lpszData = new TCHAR[dwSize];

        // Try the call again.
        goto retry;
    }
    else
    {
        // Insert error handling code.
    }
}
else
{
    // Insert code to display the cookie data.

    // Release the memory allocated for the buffer.
    delete[]lpszData;
}
```



### <a name="setting-a-cookie"></a><span data-ttu-id="0429a-124">Настройка файла cookie</span><span class="sxs-lookup"><span data-stu-id="0429a-124">Setting a Cookie</span></span>

<span data-ttu-id="0429a-125">[**Интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) используется для задания файла cookie по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="0429a-125">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) is used to set a cookie on the specified URL.</span></span> <span data-ttu-id="0429a-126">[**Интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) может создавать как постоянные, так и сеансовые файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="0429a-126">[**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) can create both persistent and session cookies.</span></span>

<span data-ttu-id="0429a-127">Постоянные файлы cookie имеют дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="0429a-127">Persistent cookies have an expiration date.</span></span> <span data-ttu-id="0429a-128">Эти файлы cookie хранятся в учетной записи Local Users в папке Users " \\ username" \\ AppData \\ роуминг \\ Microsoft \\ Windows \\ cookies, а пользователь \\ "Username" \\ AppData \\ роуминг \\ Microsoft \\ Windows \\ cookies \\ Low каталог для приложений, работающих с низкими привилегиями.</span><span class="sxs-lookup"><span data-stu-id="0429a-128">These cookies are stored in the local users account under Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies directory, and the Users\\"username"\\AppData\\Roaming\\Microsoft\\Windows\\Cookies\\Low directory for applications running under low privileges.</span></span>

<span data-ttu-id="0429a-129">Файлы cookie сеанса хранятся в памяти и доступны только создавшему их процессу.</span><span class="sxs-lookup"><span data-stu-id="0429a-129">Session cookies are stored in memory and can be accessed only by the process that created them.</span></span>

<span data-ttu-id="0429a-130">Данные для файла cookie должны быть в формате:</span><span class="sxs-lookup"><span data-stu-id="0429a-130">The data for the cookie should be in the format:</span></span>

``` syntax
NAME=VALUE
```

<span data-ttu-id="0429a-131">Для даты окончания срока действия формат должен быть следующим:</span><span class="sxs-lookup"><span data-stu-id="0429a-131">For the expiration date, the format must be:</span></span>

``` syntax
DAY, DD-MMM-YYYY HH:MM:SS GMT
```

<span data-ttu-id="0429a-132">ДЕНЬ — это 3-буквенная аббревиатура дня недели, дд — это день месяца, MMM — это трехзначный аббревиатура месяца, гггг — год, а чч: мм: СС — время суток в воинское время.</span><span class="sxs-lookup"><span data-stu-id="0429a-132">DAY is the three-letter abbreviation for the day of the week, DD is the day of the month, MMM is the three-letter abbreviation for the month, YYYY is the year, and HH:MM:SS is the time of the day in military time.</span></span>

<span data-ttu-id="0429a-133">В следующем примере показаны два вызова [**интернетсеткукие**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span><span class="sxs-lookup"><span data-stu-id="0429a-133">The following example demonstrates two calls to [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea).</span></span> <span data-ttu-id="0429a-134">Первый вызов создает файл cookie сеанса, а второй создает постоянный файл cookie.</span><span class="sxs-lookup"><span data-stu-id="0429a-134">The first call creates a session cookie and the second creates a persistent cookie.</span></span>


```C++
BOOL bReturn;

// Create a session cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
            TEXT("TestData = Test"));

// Create a persistent cookie.
bReturn = InternetSetCookie(TEXT("https://www.adventure_works.com"), NULL,
           TEXT("TestData = Test; expires = Sat,01-Jan-2000 00:00:00 GMT"));

```



> [!Note]  
> <span data-ttu-id="0429a-135">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="0429a-135">WinINet does not support server implementations.</span></span> <span data-ttu-id="0429a-136">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="0429a-136">In addition, it should not be used from a service.</span></span> <span data-ttu-id="0429a-137">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="0429a-137">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 