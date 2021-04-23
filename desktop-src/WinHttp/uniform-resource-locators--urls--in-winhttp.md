---
description: URL-адрес — это компактное представление расположения и метода доступа для ресурса, расположенного в Интернете.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: Универсальные указатели ресурсов (URL-адреса) в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080592"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a><span data-ttu-id="a85d8-103">Универсальные указатели ресурсов (URL-адреса) в WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a85d8-103">Uniform Resource Locators (URLs) in WinHTTP</span></span>

<span data-ttu-id="a85d8-104">URL-адрес — это компактное представление расположения и метода доступа для ресурса, расположенного в Интернете.</span><span class="sxs-lookup"><span data-stu-id="a85d8-104">A URL is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="a85d8-105">Каждый URL-адрес состоит из схемы (HTTP, HTTPS, FTP или gopher) и строки, зависящей от схемы.</span><span class="sxs-lookup"><span data-stu-id="a85d8-105">Each URL consists of a scheme (HTTP, HTTPS, FTP, or Gopher) and a scheme-specific string.</span></span> <span data-ttu-id="a85d8-106">Эта строка может также содержать сочетание пути к каталогу, строки поиска или имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="a85d8-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="a85d8-107">Функции служб Microsoft Windows HTTP (WinHTTP) обеспечивают возможность создания, объединения, разбиения на себя и канонизировать URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="a85d8-107">The Microsoft Windows HTTP Services (WinHTTP) functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="a85d8-108">Дополнительные сведения см. в статьях [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [универсальные указатели ресурсов](https://www.ietf.org/rfc/rfc1738.txt) и [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [универсальные идентификаторы ресурсов (URI): универсальный синтаксис](https://www.ietf.org/rfc/rfc1738.txt).</span><span class="sxs-lookup"><span data-stu-id="a85d8-108">For more information, see [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) and [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span></span>

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="a85d8-109">Что такое канонический URL-адрес?</span><span class="sxs-lookup"><span data-stu-id="a85d8-109">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="a85d8-110">Заданный синтаксис и семантика URL-адресов оставляет место для вариации и ошибок.</span><span class="sxs-lookup"><span data-stu-id="a85d8-110">The specified syntax and semantics of URLs leaves room for variation and error.</span></span> <span data-ttu-id="a85d8-111">Каноническая обработка — это процесс нормализации фактического URL-адреса в правильную, стандартную, каноническую форму.</span><span class="sxs-lookup"><span data-stu-id="a85d8-111">Canonicalization is the process of normalizing an actual URL into a correct, standard, "canonical" form.</span></span>

<span data-ttu-id="a85d8-112">Это включает в себя кодирование некоторых символов в виде escape-последовательности.</span><span class="sxs-lookup"><span data-stu-id="a85d8-112">This involves coding some characters as "escape sequences."</span></span> <span data-ttu-id="a85d8-113">Буквенно-цифровые символы США и ASCII не должны кодироваться (цифры 0-9, прописные буквы A – Z и строчные буквы a – z).</span><span class="sxs-lookup"><span data-stu-id="a85d8-113">Alphanumeric US-ASCII characters need not be encoded (the digits 0-9, the capital letters A-Z, and the lowercase letters a-z).</span></span> <span data-ttu-id="a85d8-114">Большинство других символов должны быть экранированными, включая управляющие символы, символ пробела, знак процента, "ненадежные символы" (<, >, ", \# , {,},, \| \\ , ^, ~,, \[ \] и") и все символы с кодовой точкой выше 127.</span><span class="sxs-lookup"><span data-stu-id="a85d8-114">Most other characters must be escaped, including control characters, the space character, the percent sign, "unsafe characters" ( <, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ' ), and all characters with a code point above 127.</span></span>

## <a name="using-the-winhttp-functions-to-handle-urls"></a><span data-ttu-id="a85d8-115">Использование функций WinHTTP для управления URL-адресами</span><span class="sxs-lookup"><span data-stu-id="a85d8-115">Using the WinHTTP Functions to Handle URLs</span></span>

<span data-ttu-id="a85d8-116">WinHTTP предоставляет две функции для обработки URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="a85d8-116">WinHTTP provides two functions for handling URLs.</span></span> <span data-ttu-id="a85d8-117">[**Винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) разделяет URL-адрес на части его компонентов, а [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) создает URL-адрес из компонентов.</span><span class="sxs-lookup"><span data-stu-id="a85d8-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separates a URL into its component parts, and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) creates a URL from components.</span></span>

### <a name="separating-urls"></a><span data-ttu-id="a85d8-118">Отделение URL-адресов</span><span class="sxs-lookup"><span data-stu-id="a85d8-118">Separating URLs</span></span>

<span data-ttu-id="a85d8-119">Функция [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) разделяет URL-адрес на части его компонентов и возвращает компоненты, указанные в структуре [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) , которая передается в функцию.</span><span class="sxs-lookup"><span data-stu-id="a85d8-119">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure that is passed to the function.</span></span>

<span data-ttu-id="a85d8-120">Компоненты, составляющие структуру [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) , — это номер схемы, имя узла, номер порта, имя пользователя, пароль, путь URL-адреса и дополнительные сведения, например параметры поиска.</span><span class="sxs-lookup"><span data-stu-id="a85d8-120">The components that make up the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure are the scheme number, host name, port number, user name, password, URL path, and additional information such as search parameters.</span></span> <span data-ttu-id="a85d8-121">Каждый компонент, за исключением схемы и номера портов, имеет строковый элемент, содержащий сведения и элемент, содержащий длину строкового элемента.</span><span class="sxs-lookup"><span data-stu-id="a85d8-121">Each component, except the scheme and port numbers, has a string member that holds the information and a member that holds the length of the string member.</span></span> <span data-ttu-id="a85d8-122">В схеме и номерах портов имеется только элемент, в котором хранится соответствующее значение. как схема, так и номер порта возвращаются для всех успешных вызовов [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span><span class="sxs-lookup"><span data-stu-id="a85d8-122">The scheme and port numbers have only a member that stores the corresponding value; both the scheme and port numbers are returned on all successful calls to [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span></span>

<span data-ttu-id="a85d8-123">Чтобы получить значение определенного компонента в структуре [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) , элементу, в котором хранится длина строки этого компонента, должно быть присвоено ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a85d8-123">To retrieve the value of a particular component in the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="a85d8-124">Строковый элемент может быть либо указателем на буфер, либо **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="a85d8-124">The string member can be either a pointer to a buffer or **NULL**.</span></span>

<span data-ttu-id="a85d8-125">Если элемент указателя содержит указатель на буфер, элемент длины строки должен содержать размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="a85d8-125">If the pointer member contains a pointer to a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="a85d8-126">Функция [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) возвращает сведения о компоненте в виде строки в буфере и сохраняет длину строки в члене длины строки.</span><span class="sxs-lookup"><span data-stu-id="a85d8-126">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="a85d8-127">Если для элемента указателя задано **значение NULL**, то элементу длины строки может быть присвоено любое ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a85d8-127">If the pointer member is set to **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="a85d8-128">Функция [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) сохраняет указатель на первый символ строки URL-адреса, который содержит сведения о компоненте, и задает длину строки, равную количеству символов в оставшейся части строки URL-адреса, относящейся к компоненту.</span><span class="sxs-lookup"><span data-stu-id="a85d8-128">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function stores a pointer to the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="a85d8-129">Все члены-указатели имеют **значение NULL** с ненулевой точкой члена, соответствующей отправной точке в строке URL.</span><span class="sxs-lookup"><span data-stu-id="a85d8-129">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="a85d8-130">Длину, хранящуюся в члене length, необходимо использовать для определения конца данных отдельного компонента.</span><span class="sxs-lookup"><span data-stu-id="a85d8-130">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="a85d8-131">Чтобы правильно инициализировать структуру [**\_ компонентов URL-адресов**](/windows/win32/api/winhttp/ns-winhttp-url_components) , элементу **двструктсизе** должен быть присвоен размер структуры [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) .</span><span class="sxs-lookup"><span data-stu-id="a85d8-131">To finish initializing the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure.</span></span>

### <a name="creating-urls"></a><span data-ttu-id="a85d8-132">Создание URL-адресов</span><span class="sxs-lookup"><span data-stu-id="a85d8-132">Creating URLs</span></span>

<span data-ttu-id="a85d8-133">Функция [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) использует сведения в описанной выше структуре [**\_ компонентов URL-адреса**](/windows/win32/api/winhttp/ns-winhttp-url_components) для создания URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a85d8-133">The [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) function uses the information in the previously described [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure to create a URL.</span></span>

<span data-ttu-id="a85d8-134">Для каждого обязательного компонента член-указатель должен содержать указатель на буфер, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="a85d8-134">For each required component, the pointer member should contain a pointer to the buffer that holds the information.</span></span> <span data-ttu-id="a85d8-135">Элемент length должен иметь нулевое значение, если элемент указателя содержит указатель на строку, завершающуюся нулем; элемент length должен быть установлен в значение длины строки, если элемент указателя содержит указатель на строку, которая не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="a85d8-135">The length member should be set to zero if the pointer member contains a pointer to a zero-terminated string; the length member should be set to the string length if the pointer member contains a pointer to a string that is not zero-terminated.</span></span> <span data-ttu-id="a85d8-136">Элемент указателя всех компонентов, которые не являются обязательными, должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a85d8-136">The pointer member of any components that are not required must be set to **NULL**.</span></span>

### <a name="sample-code"></a><span data-ttu-id="a85d8-137">Пример кода</span><span class="sxs-lookup"><span data-stu-id="a85d8-137">Sample code</span></span>

<span data-ttu-id="a85d8-138">В следующем примере кода показано, как использовать [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) и [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) для РАЗГРУППИРОВАНИЯ существующего URL-адреса, изменения одного из его компонентов и его сборки в новый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a85d8-138">The following sample code shows how to use the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) to disassemble an existing URL, modify one of its components, and reassemble it into a new URL.</span></span>


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



